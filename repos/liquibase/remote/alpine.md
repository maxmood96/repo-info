## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:8544830e4ca411eff42eb176feeba1b404f022df03fada5d7f1243e5613bbba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4c3e1a080bc81fa4240fd72c354596aa9035b18ae1d11f5309a81761e0372ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428538737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7b5749651c357c25993d3697b04ef5fa5b834c046760608a0d4536d794fbfe`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d254e74249fcd7b94a1781e88f1a6f82a7374fa38534597aa8ee73acc6b12d`  
		Last Modified: Tue, 03 Jun 2025 13:43:04 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa601d9e14ea7319081e6f48f04318cfb467678483e4eb561dd15c6c000ed02`  
		Last Modified: Tue, 03 Jun 2025 13:43:09 GMT  
		Size: 67.8 MB (67802051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f4f98b98e0507c8ef049e6fdc0fc8f4f2f478ab1e15be6b91e709938ec82a0`  
		Last Modified: Tue, 03 Jun 2025 13:43:20 GMT  
		Size: 353.7 MB (353659617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd18ba5867df0761825b305d7ba21b9872705937388519a51ad1329cb53d1f6c`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 3.4 MB (3433209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac55a4e3432c438a4f536d8321a94946d57d9b5824501bf61b37b901169344`  
		Last Modified: Tue, 03 Jun 2025 13:43:07 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa192255813780f3a510a1b0b662e05189ff63a6f1ddb944b58aae60cdf6fa52`  
		Last Modified: Tue, 03 Jun 2025 13:43:08 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:320a5a919092cea878a339300632114dee3cb4852d0982765a224c5791b9a63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.9 KB (424950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c0383adc941b49fcaf669264535721596363830e5377067e400a337164ace3`

```dockerfile
```

-	Layers:
	-	`sha256:6779fcfccf29fba7d611a59c6a302f2d36f8ffd99ccd7b0c7e93b181855567f3`  
		Last Modified: Wed, 04 Jun 2025 00:04:44 GMT  
		Size: 403.2 KB (403239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1393290584387fe56550a652f4a981566d37297b4d14f5ecce2866124751255`  
		Last Modified: Wed, 04 Jun 2025 00:04:44 GMT  
		Size: 21.7 KB (21711 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:5df3fe840d73b107b6091a70c051919c25807812405031f325c52f22d51a1901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.6 MB (427626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3b0f528bb29c9d8e983d8da8031c676143f017cf006c9bf956e36a288e1aa2`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d960cdd0c49e3498bf6ec7d87b10dad4343563e53b9d8035d65c95c55c52999`  
		Last Modified: Tue, 03 Jun 2025 15:03:02 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925c4a78c555ba3c950941e6d6271896da57b0ddefa6e1c39a006da828657e78`  
		Last Modified: Tue, 03 Jun 2025 15:03:06 GMT  
		Size: 66.8 MB (66799294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9a29829ca0505af0c82a9601997eaf320d57e44e1a101dde1ee080157a70a`  
		Last Modified: Tue, 03 Jun 2025 15:03:25 GMT  
		Size: 353.7 MB (353659532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac9a8ecf3de910c8dad2c8db151cfb2ea7644281a2e5c4e346d19fb363bd2c0`  
		Last Modified: Tue, 03 Jun 2025 15:03:05 GMT  
		Size: 3.2 MB (3173107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0d2579a1fe9eb19872234ce6821951463ced6acccd74269887d5e646a54856`  
		Last Modified: Tue, 03 Jun 2025 15:03:06 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d372df514f79ee87a3777443c33566eb23a953b6f7af8a4f77fe316d304b83b`  
		Last Modified: Tue, 03 Jun 2025 15:03:07 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:a2ba65aaa27cd37509f5c48e4d79ad933b55d857b0b3615510dfb819cd69e81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.3 KB (424333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1708af05fefc0c6be3e00a92e2ab51966d3aef47cfb298abc45fcc5eb99fc70`

```dockerfile
```

-	Layers:
	-	`sha256:de4ebc5acfd594b876bcf89cb72433b4b269d9b314403a4e64410bb4ea06ab0f`  
		Last Modified: Wed, 04 Jun 2025 00:04:49 GMT  
		Size: 402.5 KB (402486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c6aef5a59e7465653b4094cc2fc207c7a0c2dacbee07b2ada9f02a5f7e820d3`  
		Last Modified: Wed, 04 Jun 2025 00:04:49 GMT  
		Size: 21.8 KB (21847 bytes)  
		MIME: application/vnd.in-toto+json

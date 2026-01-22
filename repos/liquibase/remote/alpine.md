## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:79faac547231dabb16dc7826dc2f1ba4c38340a64394a25e5c5fc47a3fdf8be4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:ddecc191930f8c219e7fdc31b70fdcf86420668b3fcb93eec00058723077776c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84029488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c540f45126bf802bed524848c3d098a9447df9f28eeb7493959ae47b5cce83`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 03 Oct 2025 18:38:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
WORKDIR /liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_VERSION=0.2.14
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 03 Oct 2025 18:38:32 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
USER liquibase:liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f67999293a8197024f11dbd624adc758381fbf4e996e6169d105b063ebfd31`  
		Last Modified: Wed, 08 Oct 2025 23:10:48 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb205342480783f5bb1e06318bdaf69160f8dcb2cc985b28fc592db0da1e4d08`  
		Last Modified: Wed, 08 Oct 2025 23:10:51 GMT  
		Size: 67.9 MB (67852201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f233e00b95593d29f2e838cabc639cda38604134af51290577d01ea67bfc3f1f`  
		Last Modified: Wed, 08 Oct 2025 23:10:49 GMT  
		Size: 8.7 MB (8688917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f991eef8b65308b0fe2f26e732900a06ea4000eb2deba2e7145f73ba938206`  
		Last Modified: Wed, 08 Oct 2025 23:10:49 GMT  
		Size: 3.7 MB (3683351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc85122cd37a70766ba8cc4c8a75b626366c8394102b12927b357587790b633`  
		Last Modified: Wed, 08 Oct 2025 23:10:49 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5362889dcfde1a1a5fc3853e8c16e58b593bdf96b9e39ce9e23decdb3a30bb8e`  
		Last Modified: Wed, 08 Oct 2025 23:10:50 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:38312fdc074a63166254eeb8e0de5ab3b287fcb4397179c585330e2228483303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.4 KB (380369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a985c65a2461f599f7f0b8cd21710929ed8392b7d65e47d546322d7a392ddb0d`

```dockerfile
```

-	Layers:
	-	`sha256:a00a34b34001a3ba504d727b96bd7dec360a2a1298408cd846357a5b90f4e9b6`  
		Last Modified: Wed, 08 Oct 2025 23:10:48 GMT  
		Size: 358.7 KB (358668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4edd144ccfa0ca865ff206366cdf6aa5c7e585c08a3f3cd5219c71dcd6022aea`  
		Last Modified: Wed, 08 Oct 2025 23:10:48 GMT  
		Size: 21.7 KB (21701 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:560aef75635ecb97933699b33fab77b1d6d37c78ea3e562cc7659e33d670601e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83040049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce0d0a46acaba0bda4738c33737c69fedf98dc6a4420b187fe533d3f2d2c225`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 03 Oct 2025 18:38:32 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
WORKDIR /liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_VERSION=0.2.14
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 03 Oct 2025 18:38:32 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
USER liquibase:liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a978978408660ba16ead2899c0e6f793d970de050dd419acdfec7e851993a1`  
		Last Modified: Wed, 08 Oct 2025 21:55:41 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f7ade868c96a1721ec2bd136fa8c8ca96903d953f2a47023d5e76c7e00939`  
		Last Modified: Wed, 08 Oct 2025 21:55:43 GMT  
		Size: 66.9 MB (66850853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59db1d4966e87df96fcd3be3db735f9bdd9fc2be1f23bb49a979957e195f8697`  
		Last Modified: Wed, 08 Oct 2025 21:55:42 GMT  
		Size: 8.7 MB (8688887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251e462f64902eae401948526149fb901280d878908bd61622306a97cd3c9067`  
		Last Modified: Wed, 08 Oct 2025 21:55:41 GMT  
		Size: 3.4 MB (3359674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9636ebc80885e4a78c48b8831830c0532a46924df556443d935cd20f6612c9`  
		Last Modified: Wed, 08 Oct 2025 21:55:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9bf3dcc1ddad0806e66e3d58fc44ee595f2c3104c548514c4245811172c682`  
		Last Modified: Wed, 08 Oct 2025 21:55:43 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:84736d7937ec99f5394a54387fe6d9192ce279fdf54b24f85687b6f4332917e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.8 KB (379753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82b6981cd20307d498c47a2121551182286bc457bc404b74bd4eb53c9f6ec95`

```dockerfile
```

-	Layers:
	-	`sha256:2954d4e0f21fc3328d6f73de8c516257b530294742f27353b80f99e6c7ac7ee1`  
		Last Modified: Wed, 08 Oct 2025 21:55:41 GMT  
		Size: 357.9 KB (357915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486135ddc79373a646134e9069e76fb309dbb74e12fbc96a05718e91b8178c79`  
		Last Modified: Wed, 08 Oct 2025 21:55:41 GMT  
		Size: 21.8 KB (21838 bytes)  
		MIME: application/vnd.in-toto+json

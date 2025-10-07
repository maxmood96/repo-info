## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:6a28538099cc0209a702facd93a0178dfa4e0374da37bed108f1422fbc0019ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:8b0ee6ef6c8d7fba373b7e4854178aa3014319436445813bda72b3bbccba2994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84026986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035afe021663fef6a7602ef254195a6f5bc72dbc286496842c0ac41237c3164e`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cc68065518cc3abf94b24ec4da2a7269968da0c6e02f03074f9f988ce45384`  
		Last Modified: Mon, 06 Oct 2025 22:59:01 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693910bd5c905f30b05b6bec598adce4da94b36a87fb3aa75d14ff0ae9bb9354`  
		Last Modified: Mon, 06 Oct 2025 22:59:09 GMT  
		Size: 67.9 MB (67852345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b47fed3900572dfe639894c778790964ab827a9450d36f098e6640aee135fb`  
		Last Modified: Mon, 06 Oct 2025 22:59:02 GMT  
		Size: 8.7 MB (8688974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546c7ada820531e5c2878224948ae42610a107005e84703ea13be2fc78390622`  
		Last Modified: Mon, 06 Oct 2025 22:59:03 GMT  
		Size: 3.7 MB (3683410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e90938d551ad1a9f60c765d428e9a6ae0dfc1d38cb754a13cd11fc7089d6787`  
		Last Modified: Mon, 06 Oct 2025 22:59:01 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75de940866e88657b99319a990ec0822be7fad8bce348ab4097d532e56f9f16a`  
		Last Modified: Mon, 06 Oct 2025 22:59:01 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:475d7f95367cb971a4f51b1fad29ba6881f600065a033ba9955a147aabd5933a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.5 KB (381452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e8177782d6f546e24af32e4b87b4e72f89ee8036ee57b140892b122932e424`

```dockerfile
```

-	Layers:
	-	`sha256:b1e5ec36d9c6df94cd4609043b9011e44030e48692a33714c95ea85dac59a291`  
		Last Modified: Tue, 07 Oct 2025 00:39:28 GMT  
		Size: 359.8 KB (359751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c85e4d8526a735b3bedaafd01e8045df69e97774cc95798fe64ced0d1b35ac74`  
		Last Modified: Tue, 07 Oct 2025 00:39:29 GMT  
		Size: 21.7 KB (21701 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:553ad3f0f90dc1d8e8b8aa40065e0a394b4f8e81c3cab98414dcb093aae1dd5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83032959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3bc78dfafaa15e27a6233239b5d235533673d677047c34c61bf8e9eecbba98`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f8cef01435a6c8143fb0ebd533596f20acfe55e312f191cc717776bc2a8923`  
		Last Modified: Mon, 06 Oct 2025 23:17:26 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af3820423212d535f855a878f38f22e2f06083c1e50c277fae99e70d8bb1dc1`  
		Last Modified: Tue, 07 Oct 2025 00:40:36 GMT  
		Size: 66.9 MB (66851007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb87cf03455349f287b757ff00558340eb927ef010256b07f55e687a0be4c2d`  
		Last Modified: Tue, 07 Oct 2025 00:40:29 GMT  
		Size: 8.7 MB (8688956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad0a1c28136f3a267388e4f6188933253b5a5dca524bc6cb63a5e7b4ef73656`  
		Last Modified: Mon, 06 Oct 2025 23:17:33 GMT  
		Size: 3.4 MB (3359679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bdbd46366c1a0a52bf60250b077cc9ca347bb78992a7687a8fca07409205c2`  
		Last Modified: Mon, 06 Oct 2025 23:17:38 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e51e43830183196a010a3d529ca6ab99ef968b73c2362501e9a002b562a44b`  
		Last Modified: Mon, 06 Oct 2025 23:17:40 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:5a1632fcec58ec34a2c09e574f627c8eee8894ef3d3c8a9f151bfe323798d9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.8 KB (380836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987cb6b7e803b41dbf7f91242cd9f3df812ae44a9d80201b6c414ae931f56282`

```dockerfile
```

-	Layers:
	-	`sha256:4e54c331a1dec5e7a801719db44e705748aaa4d21c4354e185bed4127140dd16`  
		Last Modified: Tue, 07 Oct 2025 00:39:32 GMT  
		Size: 359.0 KB (358998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4c084543605a7335724a44cfbfcfb00e6d696e732b81ab6980c50c3cc04e68`  
		Last Modified: Tue, 07 Oct 2025 00:39:33 GMT  
		Size: 21.8 KB (21838 bytes)  
		MIME: application/vnd.in-toto+json

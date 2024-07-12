## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:6f3f536745f8aaf00d28de7e9830966e25690089dfe45226c3100c3b51f2cc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:134ef21c61c8787f31ecd96891af0ff7efb01308168061e56db116dc258d7ec1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180505939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afcf6ff2f06e94c3770f86d7bdd54cbb2563ac5fd52a56ddd6c3f6a006b4ade9`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 18:21:27 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Jul 2024 18:21:31 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Fri, 12 Jul 2024 18:21:32 GMT
WORKDIR /liquibase
# Fri, 12 Jul 2024 18:21:32 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Fri, 12 Jul 2024 18:21:32 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Fri, 12 Jul 2024 18:21:38 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Jul 2024 18:21:38 GMT
ARG LPM_VERSION=0.2.7
# Fri, 12 Jul 2024 18:21:38 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Fri, 12 Jul 2024 18:21:39 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Fri, 12 Jul 2024 18:21:40 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Jul 2024 18:21:41 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Jul 2024 18:21:41 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Jul 2024 18:21:41 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Jul 2024 18:21:41 GMT
USER liquibase:liquibase
# Fri, 12 Jul 2024 18:21:41 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Jul 2024 18:21:41 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df27c7e20ce434250255580c31bd093c7031ca8ce846b4aff2835d2d63c03c89`  
		Last Modified: Fri, 12 Jul 2024 18:22:36 GMT  
		Size: 981.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48513795e3273d89f5688201730d22f05de424e9cb0d486826197dce225cf3db`  
		Last Modified: Fri, 12 Jul 2024 18:22:43 GMT  
		Size: 62.6 MB (62554180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083617273bd2156108ccdbe62fc3dadadc4c5fbf35de7dcef12adbc187bd58e7`  
		Last Modified: Fri, 12 Jul 2024 18:22:39 GMT  
		Size: 108.2 MB (108176095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ccbb48e4a6ea8b71b40d378fbeb1ac8edd8b953a6e3becfa416c19ef57db3b`  
		Last Modified: Fri, 12 Jul 2024 18:22:35 GMT  
		Size: 6.2 MB (6150184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab97fa4f1da1e4556fc1b78cdbdf2dc2c40dd417da5f26b8519e780d6c9bf26`  
		Last Modified: Fri, 12 Jul 2024 18:22:34 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c1ef6a4e1155cf32481f9ecb69b075580d23d62f569652233a0ae3dbe0e5a5`  
		Last Modified: Fri, 12 Jul 2024 18:22:34 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:36ace46dae2c3a3b793e377a7118692bc3e933c648391b108e355783a40bea77
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179563631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce4d8f11745508746aec181fd756c471e36c80171200c391b056270b8b384bf`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:06:43 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Thu, 20 Jun 2024 19:06:46 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Thu, 20 Jun 2024 19:06:47 GMT
WORKDIR /liquibase
# Thu, 20 Jun 2024 19:06:47 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Thu, 20 Jun 2024 19:06:47 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Thu, 20 Jun 2024 19:06:53 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 21 Jun 2024 21:39:54 GMT
ARG LPM_VERSION=0.2.6
# Fri, 21 Jun 2024 21:39:54 GMT
ARG LPM_SHA256=0e1df6b8daf9d53a2d1d90fa8e48abbcbb8e885d249de7a09879a3a0276bebdf
# Fri, 21 Jun 2024 21:39:54 GMT
ARG LPM_SHA256_ARM=b1f6d5c8b21353b213ef828849c3d767d4214e13e8c0f4fbadd038c96ef93389
# Fri, 21 Jun 2024 21:39:56 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=0e1df6b8daf9d53a2d1d90fa8e48abbcbb8e885d249de7a09879a3a0276bebdf LPM_SHA256_ARM=b1f6d5c8b21353b213ef828849c3d767d4214e13e8c0f4fbadd038c96ef93389 LPM_VERSION=0.2.6
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 21 Jun 2024 21:39:56 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 21 Jun 2024 21:39:56 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 21 Jun 2024 21:39:56 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 21 Jun 2024 21:39:56 GMT
USER liquibase:liquibase
# Fri, 21 Jun 2024 21:39:57 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 21:39:57 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4406234da3a5998e3d1445fd0eb47ad428a631f09e763a640dbe17d75c6c6`  
		Last Modified: Thu, 20 Jun 2024 19:07:11 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7432ddf70a827b50f9b31076dc5cca2188f6a0569ff3f6b6df5f0eb112bbee`  
		Last Modified: Thu, 20 Jun 2024 19:07:16 GMT  
		Size: 62.3 MB (62268169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f0a72bb2023e4e7ed1c0d0c0d5e048f233644e1176f1c73b1b33e8b74e0913`  
		Last Modified: Thu, 20 Jun 2024 19:07:14 GMT  
		Size: 108.2 MB (108176266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c6cd7c0a29da0e46b25d0378b7cfdcd039de60b957cb5bb556c4efa1e6feee`  
		Last Modified: Fri, 21 Jun 2024 21:40:19 GMT  
		Size: 5.8 MB (5760081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65937131da85e732e7cede41536b9136f784ad21472dd314ec6dd7707972b497`  
		Last Modified: Fri, 21 Jun 2024 21:40:19 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9967525769939aef973694b3de99ceec7088ceba4e28cb8aa0a42fc8787c2ac2`  
		Last Modified: Fri, 21 Jun 2024 21:40:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

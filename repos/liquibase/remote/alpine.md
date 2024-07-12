## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:78801126bd9ed605e19736123d6afcf51fc52b258b9b6fdeec3316a97de37bf2
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
$ docker pull liquibase@sha256:a0b6a62a18ac0f036de9b745d0bb3216f6107f74ec6dea158463ef2c4cb6e048
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180278155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64c10379c2f7b20140548a40517bd0e6b3975ad60f9e8cd1fadf50c2784066c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 18:41:33 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Jul 2024 18:41:36 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Fri, 12 Jul 2024 18:41:38 GMT
WORKDIR /liquibase
# Fri, 12 Jul 2024 18:41:38 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Fri, 12 Jul 2024 18:41:38 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Fri, 12 Jul 2024 18:41:43 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Jul 2024 18:41:44 GMT
ARG LPM_VERSION=0.2.7
# Fri, 12 Jul 2024 18:41:44 GMT
ARG LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1
# Fri, 12 Jul 2024 18:41:44 GMT
ARG LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665
# Fri, 12 Jul 2024 18:41:46 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=e831120c566c76a427c6d3489cd62d5447322444399393e3ef304db0c036c4a1 LPM_SHA256_ARM=720afb6bafb987ab502b86682f410d0e19da45fdf0119d947ed7bfa4e6a02665 LPM_VERSION=0.2.7
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Jul 2024 18:41:46 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Jul 2024 18:41:46 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Jul 2024 18:41:46 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Jul 2024 18:41:46 GMT
USER liquibase:liquibase
# Fri, 12 Jul 2024 18:41:46 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Jul 2024 18:41:46 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef1f3fa20c81c87527d5311b77703259dfda897b27c7cc9fb33dcceb1080274`  
		Last Modified: Fri, 12 Jul 2024 18:42:46 GMT  
		Size: 981.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255f1ede0cd85174c3fb33950f7b87ce1fc0bb8f40fab10cbbc471c179d9cb3a`  
		Last Modified: Fri, 12 Jul 2024 18:42:51 GMT  
		Size: 62.3 MB (62252188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa2a18da1970e7c2709e49c0196719dbe2c9ef4e382a7f0ff898074e0d285ec`  
		Last Modified: Fri, 12 Jul 2024 18:42:49 GMT  
		Size: 108.2 MB (108175846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710a030dd91a935af4f4ad44ec63070bdfc7d68ce0c6787504373a5002d99dbf`  
		Last Modified: Fri, 12 Jul 2024 18:42:45 GMT  
		Size: 5.8 MB (5759684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6e2e016bfaff83c951c418f1b58b782b2330a3abdfaf9d1d1053835002f90a`  
		Last Modified: Fri, 12 Jul 2024 18:42:44 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b69c7d5a7e1aa4aa529d88949d4eff125a604ec2d58e4e375a5396cc1c730c8`  
		Last Modified: Fri, 12 Jul 2024 18:42:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

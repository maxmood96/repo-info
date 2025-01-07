## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:d4bdcbba195c8f7e379ea26f96f5d597b403c779d2f67f5bca92b43097be710a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:a45815309b0e63491194de8a9e223aa9d2d89affe6185b0542554247076abc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229919385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53baa893085ccfaf230c1ed8fc2620de5c88f581f4feb5778fe59c738072e73d`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 07 Nov 2024 14:28:00 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
WORKDIR /liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LIQUIBASE_VERSION=4.30.0
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_VERSION=0.2.8
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 07 Nov 2024 14:28:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
USER liquibase:liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9de46f2186c5884dc9f9dbb14ba51023d93625570f404c07bf13077ffa65be`  
		Last Modified: Tue, 07 Jan 2025 03:33:15 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5569c57b44f9c47dbf8483b51e94c0063fce0cf00b11b64cffc5a73bf0ffeb`  
		Last Modified: Tue, 07 Jan 2025 03:33:16 GMT  
		Size: 62.6 MB (62604508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf3f4a35bb24f9625db88c0e66ee1d7b5986a8f5d2dfc7886dbd878a7c15350`  
		Last Modified: Tue, 07 Jan 2025 03:33:17 GMT  
		Size: 160.5 MB (160458759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75db1f4427db6246cbec05cdceb89f23fd825cda31b50166e83a79e1a15ba450`  
		Last Modified: Tue, 07 Jan 2025 03:33:15 GMT  
		Size: 3.2 MB (3240454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cae38520d7ca9b2cf97dc3d29b05b889ba95f9c61b3da15df0322f778fa3b4`  
		Last Modified: Tue, 07 Jan 2025 03:33:16 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27be825a3831f0bde63c3760584bd2c21d4e9ae1e6b76421020d3aa583c71e5f`  
		Last Modified: Tue, 07 Jan 2025 03:33:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:4ccd388360bfb465d0f84b8c6c95bc385c43f872f9dbf08d63b83ae0a2846e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.6 KB (393636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9b2900efe1fa874a5a00e13ff6e4f8d0d1a906903fb7c35bb5cdee15f89669`

```dockerfile
```

-	Layers:
	-	`sha256:2c740ea18834795afb54b1cec30e67345abcedea7f6e1e898311e3cbe7b70b2e`  
		Last Modified: Tue, 07 Jan 2025 03:33:15 GMT  
		Size: 372.4 KB (372372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4be990a6eb5308f5128a69b4a55a56e405bf6c878d306d0deb87ac5a5451f19`  
		Last Modified: Tue, 07 Jan 2025 03:33:15 GMT  
		Size: 21.3 KB (21264 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:7affa3d13963881c75d484e7559181dc6c87f994ae5613cef2b39cb39b6561d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229855537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3238bcbdcd0d6b2e107778bbc42859530a5842d8960d4b658c649753822e40`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 07 Nov 2024 14:28:00 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
WORKDIR /liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LIQUIBASE_VERSION=4.30.0
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_VERSION=0.2.8
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 07 Nov 2024 14:28:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
USER liquibase:liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39251f14351216880df5cf91e29ae0efd884c6eb0c5a0fdfb7b66de23f8bf8e`  
		Last Modified: Tue, 07 Jan 2025 08:38:41 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d36771de0794a5a2a9ab09d9fdc1e289300c2a13142ccc5f72f3ac75a94da9`  
		Last Modified: Tue, 07 Jan 2025 08:38:43 GMT  
		Size: 62.3 MB (62316487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35abeacdcf10e229ed75722ef3993c8d54c23f7582b78e4f79049d409c408fb4`  
		Last Modified: Tue, 07 Jan 2025 08:38:45 GMT  
		Size: 160.5 MB (160458808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab93bfd9cb93538e6140ca7ab88fa00ded6ef820538ec31d6bbcb4cbb33f613`  
		Last Modified: Tue, 07 Jan 2025 08:38:42 GMT  
		Size: 3.0 MB (2991891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c26b0c429bee5bb49cdb9cfb2109d4ac72309d74091c8aa199526975e9858a7`  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7101e72794a7960a45d70930f4a6ffebd3f2374dd700fd75fe74b5e1302b2ad`  
		Last Modified: Tue, 07 Jan 2025 08:38:43 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:647b07079a4f2bfb1994bbf4b1869e5fa9ca915eac49d9bab3a9b9ef8558537d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.0 KB (393020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa544e65d9125065e58076e8665a39a2289cb047da63e536d3ae9d19a7b0a3bc`

```dockerfile
```

-	Layers:
	-	`sha256:f73782cbe08adf3614b94f37160204fff3494a152db31a30a191a9c31f10e4e2`  
		Last Modified: Tue, 07 Jan 2025 08:38:41 GMT  
		Size: 371.6 KB (371619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acf0da6886ac56b77c16f7783446d48c215b5e0c1cd33da8c25ccf818f491b4c`  
		Last Modified: Tue, 07 Jan 2025 08:38:41 GMT  
		Size: 21.4 KB (21401 bytes)  
		MIME: application/vnd.in-toto+json

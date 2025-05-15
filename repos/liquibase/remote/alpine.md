## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:2af38d00ae3fa226c56e1226c340636db6baa5657c661d7eaf0c298dbad7d487
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:ce70f60df530a1a9e875f8cdfb4e8db9816d8ce0fdfb5820c6e7af4e12354303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.7 MB (421672197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c5ce234ca9319f6bb3558eb03318f25c199aa8285f4f3d4d000bb9f444429b`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Feb 2025 16:29:17 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
WORKDIR /liquibase
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LIQUIBASE_VERSION=4.31.1
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LB_SHA256=0555808b59941d497f0c1114c3f2225698afde11c60d191c88e449506a60a3ea
# Mon, 17 Feb 2025 16:29:17 GMT
# ARGS: LIQUIBASE_VERSION=4.31.1 LB_SHA256=0555808b59941d497f0c1114c3f2225698afde11c60d191c88e449506a60a3ea
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LPM_VERSION=0.2.8
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Mon, 17 Feb 2025 16:29:17 GMT
# ARGS: LIQUIBASE_VERSION=4.31.1 LB_SHA256=0555808b59941d497f0c1114c3f2225698afde11c60d191c88e449506a60a3ea LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
ENV LIQUIBASE_HOME=/liquibase
# Mon, 17 Feb 2025 16:29:17 GMT
ENV DOCKER_LIQUIBASE=true
# Mon, 17 Feb 2025 16:29:17 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
COPY liquibase.docker.properties ./ # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
USER liquibase:liquibase
# Mon, 17 Feb 2025 16:29:17 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Mon, 17 Feb 2025 16:29:17 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fda8e65817fdabae3905b4eceac0d79476ac411cc619e7f03bad39ae47a52af`  
		Last Modified: Tue, 18 Feb 2025 21:29:57 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ec3a2b568ee5bad29ff4d7f6da0734c73bdebfb0cf32135ea09e962347a020`  
		Last Modified: Tue, 18 Feb 2025 21:30:01 GMT  
		Size: 62.8 MB (62774429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b2d09ce8b5fb273b934e945cec6e2a487be8560226553a8b2e5565638c3b0c`  
		Last Modified: Wed, 19 Feb 2025 03:04:49 GMT  
		Size: 352.0 MB (352012637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b34b2301eed52e77b2a3a38a0e0b99a192d000c877dba94b1aa24eab80bd030`  
		Last Modified: Tue, 18 Feb 2025 21:29:58 GMT  
		Size: 3.2 MB (3241274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd3208468c88e63402cd4670456d8d909d05a5a3c752dae9b52893f30202c25`  
		Last Modified: Tue, 18 Feb 2025 21:30:00 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd4f5605ada6a0ef3a3ead95c0e5a6ca35410a240a6767b7add6715119b8414`  
		Last Modified: Tue, 18 Feb 2025 21:30:01 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:fb75438068bd24b2058abe6ee9b159d8fc3472f93eefa4b4800536d5e35f71eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa37033ca17afde6ddfb44658ef37edb7c9c8610b3292ca15ed2d4b1acf811e`

```dockerfile
```

-	Layers:
	-	`sha256:58849b11b18ceb2cafd1ab052641bb863b4ff88dfb6c634118c9badd6842b294`  
		Last Modified: Wed, 19 Feb 2025 01:39:20 GMT  
		Size: 385.1 KB (385086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf79a548d252a4c48ebe60fa561926edbc91af9387f50520aaf2be5106f064ae`  
		Last Modified: Wed, 19 Feb 2025 01:39:20 GMT  
		Size: 21.2 KB (21248 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:75594912e9ceb6e05f05c2a3580d801e1a29e80b5cc689ea750595adddd14476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.0 MB (420971517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddf699a4bf48b9c53993e0fc51cfa16552c092659bfd8887298bdf9348d33e2`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Feb 2025 16:29:17 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
WORKDIR /liquibase
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LIQUIBASE_VERSION=4.31.1
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LB_SHA256=0555808b59941d497f0c1114c3f2225698afde11c60d191c88e449506a60a3ea
# Mon, 17 Feb 2025 16:29:17 GMT
# ARGS: LIQUIBASE_VERSION=4.31.1 LB_SHA256=0555808b59941d497f0c1114c3f2225698afde11c60d191c88e449506a60a3ea
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LPM_VERSION=0.2.8
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Mon, 17 Feb 2025 16:29:17 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Mon, 17 Feb 2025 16:29:17 GMT
# ARGS: LIQUIBASE_VERSION=4.31.1 LB_SHA256=0555808b59941d497f0c1114c3f2225698afde11c60d191c88e449506a60a3ea LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
ENV LIQUIBASE_HOME=/liquibase
# Mon, 17 Feb 2025 16:29:17 GMT
ENV DOCKER_LIQUIBASE=true
# Mon, 17 Feb 2025 16:29:17 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
COPY liquibase.docker.properties ./ # buildkit
# Mon, 17 Feb 2025 16:29:17 GMT
USER liquibase:liquibase
# Mon, 17 Feb 2025 16:29:17 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Mon, 17 Feb 2025 16:29:17 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d80fac97bd8e989f5679486996280eb8838fe67583da9b3c5f8bbad00ca0b3`  
		Last Modified: Sat, 15 Feb 2025 05:03:27 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f90999cbb6c5d850cf2b2349bfc316f2389ec487c7f90e511751acc8822080`  
		Last Modified: Sat, 15 Feb 2025 05:03:29 GMT  
		Size: 62.0 MB (61972256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b499162af7bac2b6c1101bf51aacfebc18dba8139cc3a66cc5cb794c953a67ba`  
		Last Modified: Wed, 19 Feb 2025 05:03:32 GMT  
		Size: 352.0 MB (352012657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dd65e14b314782e127058e32c587563b7b341f541ac251d81666ecbe6b66ed`  
		Last Modified: Tue, 18 Feb 2025 21:33:44 GMT  
		Size: 3.0 MB (2991967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bf911c96ae1306c1a710c6bd760cbfd01193d07541b783a08086c0baaed2d7`  
		Last Modified: Tue, 18 Feb 2025 21:33:43 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7d9a384b196b426e5ceeddd74709b75e0ae3c3f4915d557e1d593ebe606658`  
		Last Modified: Tue, 18 Feb 2025 21:33:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:a43c7c17c582d230eb865e131ddbc34ddabb32ffe949bfdc620576f7ecf30478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.7 KB (405718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcd02409484bcc032616bac42391f6bdcc41f6ee27baecb721690f3f9c9aeac`

```dockerfile
```

-	Layers:
	-	`sha256:37e3bd2be6f627174d2aafaa1a720a6ca9234f23a57919eda7fb197f4a2713bc`  
		Last Modified: Tue, 18 Feb 2025 22:39:27 GMT  
		Size: 384.3 KB (384333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:192a7ff2975ceb58eed4cda5c02a2b640be5cb5b731c38a5114dd9fd09dff79e`  
		Last Modified: Tue, 18 Feb 2025 22:39:27 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

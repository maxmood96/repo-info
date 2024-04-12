## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:3569a5194a22fcd31d95ffd183f3c86b036ea893a79dc79aab394cea9eb3903c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:8e83243d494f413e5d1dd537beb2ee8a5c3f3236a6fc860caa6d95ce7f87bd4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179118630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60f98847f0d02b37c0091d18ae1546c59490ef6e609604eac0640ae9c9b3a70`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 21:53:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Apr 2024 21:53:16 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Fri, 12 Apr 2024 21:53:17 GMT
WORKDIR /liquibase
# Fri, 12 Apr 2024 21:53:17 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 12 Apr 2024 21:53:17 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 12 Apr 2024 21:53:23 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Apr 2024 21:53:23 GMT
ARG LPM_VERSION=0.2.4
# Fri, 12 Apr 2024 21:53:23 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 12 Apr 2024 21:53:23 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 12 Apr 2024 21:53:25 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Apr 2024 21:53:25 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Apr 2024 21:53:25 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Apr 2024 21:53:25 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Apr 2024 21:53:26 GMT
USER liquibase:liquibase
# Fri, 12 Apr 2024 21:53:26 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 21:53:26 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628b26e1b7d5e53dc3f871fbd5207d7b0dbed83f5652c6b593e7523f327b0995`  
		Last Modified: Fri, 12 Apr 2024 21:53:58 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16375c5e067803a594c16a34069a277129130d10c6e9f5e0dbf7a3487d94215`  
		Last Modified: Fri, 12 Apr 2024 21:54:03 GMT  
		Size: 62.6 MB (62551332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80890c3d38ea6a223d979b84509075148311447fc8ac6600c294ddfae065f4d1`  
		Last Modified: Fri, 12 Apr 2024 21:54:01 GMT  
		Size: 107.2 MB (107167151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8feb059297540b79a709e55c1606d0df0b30c4353b35114585c6614198663e`  
		Last Modified: Fri, 12 Apr 2024 21:53:56 GMT  
		Size: 6.0 MB (5989458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74eff2b7e0ed7e98c8fe6ca67e84b2c306d9846c1805984d30224a9c36c3360`  
		Last Modified: Fri, 12 Apr 2024 21:53:55 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e5e492ea3d14e8820abf9031e78088571b07f8a8e98d80c2b21e994283ef36`  
		Last Modified: Fri, 12 Apr 2024 21:53:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:5d040853b474bcc42db35dfe65297d1cc95cc475ada0d5afbfd6323fc49f8dd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178376991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7ee5e4a96c378d24640a5b7623ab2ac82bba61db9c3e9c486ae942cb10ede6`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 22:09:41 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase
# Fri, 12 Apr 2024 22:09:43 GMT
RUN apk add --no-cache openjdk17-jre-headless bash
# Fri, 12 Apr 2024 22:09:45 GMT
WORKDIR /liquibase
# Fri, 12 Apr 2024 22:09:45 GMT
ARG LIQUIBASE_VERSION=4.27.0
# Fri, 12 Apr 2024 22:09:45 GMT
ARG LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0
# Fri, 12 Apr 2024 22:09:50 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Fri, 12 Apr 2024 22:09:50 GMT
ARG LPM_VERSION=0.2.4
# Fri, 12 Apr 2024 22:09:51 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Fri, 12 Apr 2024 22:09:51 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Fri, 12 Apr 2024 22:09:52 GMT
# ARGS: LB_SHA256=50d89e1fc10249bf198f1a8ff2d81fd0b68e6ca0805db28a94d38649784d82f0 LIQUIBASE_VERSION=4.27.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Fri, 12 Apr 2024 22:09:53 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 12 Apr 2024 22:09:53 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Fri, 12 Apr 2024 22:09:53 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Fri, 12 Apr 2024 22:09:53 GMT
USER liquibase:liquibase
# Fri, 12 Apr 2024 22:09:53 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 22:09:53 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5cf91af4c3b9ba459a6c2e1e4720bb24d515e7e1590061221774c5afc05741`  
		Last Modified: Fri, 12 Apr 2024 22:10:27 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25670433c04b1b51be1d83e9471b255315d5855735fdb5c478de779fc4d36c1a`  
		Last Modified: Fri, 12 Apr 2024 22:10:32 GMT  
		Size: 62.2 MB (62247991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a0662a2f48ebe9e1417bf734bd23a1364ed6ff98e24ba92df730f7103e4a87`  
		Last Modified: Fri, 12 Apr 2024 22:10:30 GMT  
		Size: 107.2 MB (107167120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5e8d1878262c3f6371355d3e70fda8d44e1160933043bf3410ad3e8c81747f`  
		Last Modified: Fri, 12 Apr 2024 22:10:26 GMT  
		Size: 5.6 MB (5612200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a4512c1e0f3ab24f8063edc55981331b296f8616aa8946db6b741c6234c38a`  
		Last Modified: Fri, 12 Apr 2024 22:10:25 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f90ac47caca49d33b4fd4a4dc651d9a11570ab8a4d7f930332efbf7cdaaf670`  
		Last Modified: Fri, 12 Apr 2024 22:10:25 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

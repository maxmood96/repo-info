## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:963cdfc009335c7abd729f09260a0a98d201b3157c2c962e7a6d0142966134ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:88df19b7563152da0f414b828779777e217c80ff3f683ad69b9d43933ceca9f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180128000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6682295d24e63bdb39f8d475a7f0ad8c5630f90434325320ba608254da5aa7ac`
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
# Thu, 23 May 2024 19:32:02 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Thu, 23 May 2024 19:32:03 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Thu, 23 May 2024 19:32:09 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 23 May 2024 19:32:09 GMT
ARG LPM_VERSION=0.2.4
# Thu, 23 May 2024 19:32:10 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Thu, 23 May 2024 19:32:10 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Thu, 23 May 2024 19:32:11 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 23 May 2024 19:32:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 23 May 2024 19:32:12 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 23 May 2024 19:32:12 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 23 May 2024 19:32:12 GMT
USER liquibase:liquibase
# Thu, 23 May 2024 19:32:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 23 May 2024 19:32:12 GMT
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
	-	`sha256:fb77b6dc6f8090ac12c00c65d6ea634c83fcd075c285fba37488551f1e81de26`  
		Last Modified: Thu, 23 May 2024 19:32:45 GMT  
		Size: 108.2 MB (108176511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2199d8266f17ac40199f63462f90edf47a3afe8a2e7e89cdeb1fedc8a06f81b3`  
		Last Modified: Thu, 23 May 2024 19:32:40 GMT  
		Size: 6.0 MB (5989466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eba3fbc1bc92c2a466e2ffebad68391b3068c1333e8f3232ce58fc669be27c7`  
		Last Modified: Thu, 23 May 2024 19:32:40 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0208ffd5550473c13ee70ef23b959d1585554899b02467f13c2a60dca99cb1`  
		Last Modified: Thu, 23 May 2024 19:32:40 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:a9e4e85203db7edab1de2e50d84f15094d7727f85d2bf20927a7cc30f637bd96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179386264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e0eeb43359bb8fcd66ab604e2623daef8e363c5bb110374ee052d27df7cf04`
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
# Thu, 23 May 2024 19:40:11 GMT
ARG LIQUIBASE_VERSION=4.28.0
# Thu, 23 May 2024 19:40:11 GMT
ARG LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8
# Thu, 23 May 2024 19:40:17 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version
# Thu, 23 May 2024 19:40:17 GMT
ARG LPM_VERSION=0.2.4
# Thu, 23 May 2024 19:40:17 GMT
ARG LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf
# Thu, 23 May 2024 19:40:17 GMT
ARG LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0
# Thu, 23 May 2024 19:40:19 GMT
# ARGS: LB_SHA256=97dd07eaca0406a09e1ae19b407eea42a7e944c7f4571922bffce71b43b75ce8 LIQUIBASE_VERSION=4.28.0 LPM_SHA256=c3ecdc0fc0be75181b40e189289bf7fdb3fa62310a1d2cf768483b34e1d541cf LPM_SHA256_ARM=375acfa1e12aa0e11c4af65e231e6471ea8d5eea465fb58b516ea2ffbd18f3e0 LPM_VERSION=0.2.4
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version
# Thu, 23 May 2024 19:40:19 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 23 May 2024 19:40:19 GMT
COPY file:de48911eb8db3870b1900fa0141e8a528d47fc7c60d29997ed293586bfaf6d64 in ./ 
# Thu, 23 May 2024 19:40:19 GMT
COPY file:e457fe6fb13404d03e09152692b0afddbaae5ccbc4b35ccc08fe2667e50bbe6a in ./ 
# Thu, 23 May 2024 19:40:19 GMT
USER liquibase:liquibase
# Thu, 23 May 2024 19:40:19 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 23 May 2024 19:40:19 GMT
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
	-	`sha256:f027e26b35951be827fa6ba9cd5c288c95b0278cafee99071b7a5e84d545176b`  
		Last Modified: Thu, 23 May 2024 19:40:49 GMT  
		Size: 108.2 MB (108176382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c3fdbcd35f6d4d362d017c99fd3299d7fbfeabf1da4a4349af7ffb5fd35e75`  
		Last Modified: Thu, 23 May 2024 19:40:46 GMT  
		Size: 5.6 MB (5612208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67678c3847b2d8a1deea4b6adbe0e398b7391d2348e18b42f88c6b8f9c1dcd7e`  
		Last Modified: Thu, 23 May 2024 19:40:45 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44b2955f385955f28c71fbe3d48fa44efb505535034afd451043327fc2e352c`  
		Last Modified: Thu, 23 May 2024 19:40:45 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

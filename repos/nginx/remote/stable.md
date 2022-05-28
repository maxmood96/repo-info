## `nginx:stable`

```console
$ docker pull nginx@sha256:5abb77348599aa4fec6fe62b0b054d06587ea43e5c5d3a29fb0d84c675b998a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `nginx:stable` - linux; amd64

```console
$ docker pull nginx@sha256:36be6b1d3477352a59dbffd660a24c7bd8617a134bd3349fd376b9df61855c1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56734295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3149f43818854f4b96a1274eabb218129b4a6f336d582faa2e27631ad5b786`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 11 May 2022 01:20:16 GMT
ADD file:4a0bb88956083aa56032fdd9601d9b66c39b18c896ba35ea33594cd75621640a in / 
# Wed, 11 May 2022 01:20:16 GMT
CMD ["bash"]
# Wed, 11 May 2022 05:04:29 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 25 May 2022 18:38:54 GMT
ENV NGINX_VERSION=1.22.0
# Wed, 25 May 2022 18:38:54 GMT
ENV NJS_VERSION=0.7.4
# Wed, 25 May 2022 18:38:54 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 25 May 2022 18:39:12 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 25 May 2022 18:39:13 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Wed, 25 May 2022 18:39:13 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Wed, 25 May 2022 18:39:13 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Wed, 25 May 2022 18:39:13 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Wed, 25 May 2022 18:39:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 May 2022 18:39:13 GMT
EXPOSE 80
# Wed, 25 May 2022 18:39:13 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 May 2022 18:39:13 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:214ca5fb90323fe769c63a12af092f2572bf1c6b300263e09883909fc865d260`  
		Last Modified: Wed, 11 May 2022 01:25:13 GMT  
		Size: 31.4 MB (31379476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cbb497c326a1773331980d6e60438ad61416e4b4f8046a49a7c81a313a5df1`  
		Last Modified: Wed, 25 May 2022 18:40:46 GMT  
		Size: 25.4 MB (25351266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c4910349a0a9c9b202313ae5e9a7e511f0425f904492117a7de1691b61f6ca`  
		Last Modified: Wed, 25 May 2022 18:40:43 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88e73a4c2d13b43c5b6d7b8e802c67b89987d572158b6564d24dc67d486c2e6`  
		Last Modified: Wed, 25 May 2022 18:40:43 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3fe55fabfa47a6537273c8f1a6cb7b3537fbde6cf838763af05c2c426b4ec5`  
		Last Modified: Wed, 25 May 2022 18:40:43 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d766a4b2ae83a715d3e525014b2dc0783d84b4b822772ab2570c314639d2f64f`  
		Last Modified: Wed, 25 May 2022 18:40:43 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; arm variant v5

```console
$ docker pull nginx@sha256:e884c46a968f64d6d736fb0df633f0940c69f1b061fbcec7e82cf1d6a6c41638
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54848103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f80ebd307cf57b8e34bd32d75113ff55fa4ff1709bee2f7fe975287c804da7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 11 May 2022 00:50:34 GMT
ADD file:72357b75d7e4546f06abf4648ab600980e742a3017f36da3c7a6c086f2f5fb56 in / 
# Wed, 11 May 2022 00:50:35 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:43:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 25 May 2022 17:59:16 GMT
ENV NGINX_VERSION=1.22.0
# Wed, 25 May 2022 17:59:17 GMT
ENV NJS_VERSION=0.7.4
# Wed, 25 May 2022 17:59:17 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 25 May 2022 18:08:04 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 25 May 2022 18:08:05 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Wed, 25 May 2022 18:08:06 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Wed, 25 May 2022 18:08:06 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Wed, 25 May 2022 18:08:06 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Wed, 25 May 2022 18:08:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 May 2022 18:08:07 GMT
EXPOSE 80
# Wed, 25 May 2022 18:08:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 May 2022 18:08:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f7b69be15db1cb94a249f74b27edd4f5e5923a8701b026179a593f6888e897aa`  
		Last Modified: Wed, 11 May 2022 01:05:51 GMT  
		Size: 28.9 MB (28921122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fe6a0fd8e3db74e08a8b8443150459c263c86de53daca8e7ddaa8389b0c62d`  
		Last Modified: Wed, 25 May 2022 18:20:17 GMT  
		Size: 25.9 MB (25923418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a790baebab792485e0a763843faa3d95ddeb1e04d577587ce28b76210ef8e698`  
		Last Modified: Wed, 25 May 2022 18:20:02 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e996e82453950b59035e36d924750b220bd86425d457a79c0b3fea6171ae16f`  
		Last Modified: Wed, 25 May 2022 18:20:02 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0925ab380ed8e72442017fbeffb6bbabb49e0b66b311b30a93d6ff5ba9bdb56f`  
		Last Modified: Wed, 25 May 2022 18:20:02 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23681a09dede74d8c66cc3bcd70d398c341a7230493829b344eb209a96dbb1e1`  
		Last Modified: Wed, 25 May 2022 18:20:02 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; arm variant v7

```console
$ docker pull nginx@sha256:53a8ea7f2bead2c66e8eccd41a3b8ab6d9b15f6537eb48c658f0fa6fe594a4e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51572058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f9e60cff9c9f01f49523b8e8f34caf765331c631dd750365a549984caff537`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 11 May 2022 01:49:07 GMT
ADD file:7c0451fffe8a520c2ab23048948d76bfe0dc0d90298c3d859279ccd8815b84f6 in / 
# Wed, 11 May 2022 01:49:08 GMT
CMD ["bash"]
# Thu, 12 May 2022 10:37:37 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 25 May 2022 18:04:48 GMT
ENV NGINX_VERSION=1.22.0
# Wed, 25 May 2022 18:04:48 GMT
ENV NJS_VERSION=0.7.4
# Wed, 25 May 2022 18:04:49 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 25 May 2022 18:13:04 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 25 May 2022 18:13:05 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Wed, 25 May 2022 18:13:05 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Wed, 25 May 2022 18:13:06 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Wed, 25 May 2022 18:13:06 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Wed, 25 May 2022 18:13:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 May 2022 18:13:07 GMT
EXPOSE 80
# Wed, 25 May 2022 18:13:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 May 2022 18:13:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:1a9427b75b1c1db800cae7a9199bb4e508702e6761b17cc904d21441df43016c`  
		Last Modified: Wed, 11 May 2022 02:04:35 GMT  
		Size: 26.6 MB (26575672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bf4f5ce45ce568fcc08c8c7e78e92de3c07a365510a68d999288644a6a4e3b`  
		Last Modified: Wed, 25 May 2022 18:41:53 GMT  
		Size: 25.0 MB (24992819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba40cf9a1597b4c91a7ead62e8c36a8ff5e15e78f00775a01d9f3b931bb6bed`  
		Last Modified: Wed, 25 May 2022 18:41:40 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debf9bc9e1513883fa44d7b861e38001e47cdf2f8e4e10cf0b1ffb47d502595b`  
		Last Modified: Wed, 25 May 2022 18:41:40 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d44a61c7f50d6bee3eaf845c3bfbfdaf4ba2d42f09d05b2dc4607223d256c5a`  
		Last Modified: Wed, 25 May 2022 18:41:40 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9840a2d9210473f06c73189343fa33775545eebe0ee503a702b0faeaeac3a48f`  
		Last Modified: Wed, 25 May 2022 18:41:40 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:8372e3c601e38dadb6041186fe9f06107bb62d756e984ffed280fb0da984ac33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.4 MB (55353975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ae714a6185508851580198821800bc281b26937210030aef8320789294b3db`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 28 May 2022 00:40:39 GMT
ADD file:55b4fe3115c684f545e4e4148c93745f12192976a08c37d090fcac708fb709a7 in / 
# Sat, 28 May 2022 00:40:39 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:52:44 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Sat, 28 May 2022 02:54:12 GMT
ENV NGINX_VERSION=1.22.0
# Sat, 28 May 2022 02:54:13 GMT
ENV NJS_VERSION=0.7.4
# Sat, 28 May 2022 02:54:14 GMT
ENV PKG_RELEASE=1~bullseye
# Sat, 28 May 2022 02:54:38 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Sat, 28 May 2022 02:54:40 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Sat, 28 May 2022 02:54:41 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Sat, 28 May 2022 02:54:42 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Sat, 28 May 2022 02:54:43 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Sat, 28 May 2022 02:54:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:54:44 GMT
EXPOSE 80
# Sat, 28 May 2022 02:54:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 28 May 2022 02:54:46 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:dc1f00a5d701e86e2cd2568b860c61b393d66be1341e7267d07e6e57448ceeba`  
		Last Modified: Sat, 28 May 2022 00:47:35 GMT  
		Size: 30.1 MB (30065728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634478c86609bedf67f343c6a89d05be46712993dd5be8387f3523ac8b53e7f3`  
		Last Modified: Sat, 28 May 2022 02:57:39 GMT  
		Size: 25.3 MB (25284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b5fa92f5dd2b734d633d33d0c88faa1ce4609d0c9dd4022d499d6cf4893c15`  
		Last Modified: Sat, 28 May 2022 02:57:35 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d048fa95de87bf428fd6268aba4ed34262ef1c7e8fc84b1f74e0c0af39082a3f`  
		Last Modified: Sat, 28 May 2022 02:57:35 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68717c705e7da471cb5544f0b0f79eb2dec9e6cd3c7283a1d76a4e3ede86bb12`  
		Last Modified: Sat, 28 May 2022 02:57:35 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e96bb3a5913408f2a6094caef0d08c489bf6c0cc65ecdc61e84896f56227ab4`  
		Last Modified: Sat, 28 May 2022 02:57:35 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; 386

```console
$ docker pull nginx@sha256:8803c2baf3ef057658ad10450753558b5762231b92d8d50809aa03ff41be0a44
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60345566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4c88555083dec9d61e4da6e2052dd108f428b06eb949ffc916c0973473d303`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 11 May 2022 01:39:14 GMT
ADD file:9eecb0fd311177f9d226e914c411aef49b5de1930e73019d2ee24afed515b5a2 in / 
# Wed, 11 May 2022 01:39:14 GMT
CMD ["bash"]
# Wed, 11 May 2022 04:43:39 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 25 May 2022 17:39:06 GMT
ENV NGINX_VERSION=1.22.0
# Wed, 25 May 2022 17:39:07 GMT
ENV NJS_VERSION=0.7.4
# Wed, 25 May 2022 17:39:08 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 25 May 2022 17:42:17 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 25 May 2022 17:42:18 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Wed, 25 May 2022 17:42:19 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Wed, 25 May 2022 17:42:20 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Wed, 25 May 2022 17:42:21 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Wed, 25 May 2022 17:42:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 May 2022 17:42:22 GMT
EXPOSE 80
# Wed, 25 May 2022 17:42:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 May 2022 17:42:24 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:91c5bdbe4bf9f1970dd54ba71e2523649adce4e5240c2ff8a87711bf389ecba3`  
		Last Modified: Wed, 11 May 2022 01:46:25 GMT  
		Size: 32.4 MB (32389776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0836bcc84b726b1fb60e3dfbdecd179e47e8265221282abe41dac33fd1e8a3`  
		Last Modified: Wed, 25 May 2022 17:54:19 GMT  
		Size: 28.0 MB (27952228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df388b515a2f3b52216b125968bbb499c2326d88b50ee695bbc82e02bce6a89`  
		Last Modified: Wed, 25 May 2022 17:54:15 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db1dffe5234ec40b2f6d4fb699c2c8e0c577599ac046f81d761eb4640879a68`  
		Last Modified: Wed, 25 May 2022 17:54:15 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b54978d96b0fcd756e0826c4de811a2c5b0e35f081bc3a15c27900bac64352c`  
		Last Modified: Wed, 25 May 2022 17:54:15 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030a5e6135c803d2e7cd3aa48f34e59a6b1caef4ef6e06c5cac53486f811a9de`  
		Last Modified: Wed, 25 May 2022 17:54:15 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; mips64le

```console
$ docker pull nginx@sha256:1ce075d0077ba3292fb52701b59799c86736dfb2b579ec07c9d6943eca76223d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56160839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4508b393fef688775032a627cbe5b98bb0306dd0392016ace61465d6b695b99`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 11 May 2022 02:23:35 GMT
ADD file:d47dce2adbc9352ef1d437730bab3b579dd8d2bf29dd60cd8a8b65396b39e36e in / 
# Wed, 11 May 2022 02:23:40 GMT
CMD ["bash"]
# Wed, 11 May 2022 04:34:44 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 25 May 2022 18:07:43 GMT
ENV NGINX_VERSION=1.22.0
# Wed, 25 May 2022 18:07:45 GMT
ENV NJS_VERSION=0.7.4
# Wed, 25 May 2022 18:07:47 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 25 May 2022 18:22:49 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 25 May 2022 18:22:52 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Wed, 25 May 2022 18:22:54 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Wed, 25 May 2022 18:22:56 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Wed, 25 May 2022 18:22:58 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Wed, 25 May 2022 18:23:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 May 2022 18:23:02 GMT
EXPOSE 80
# Wed, 25 May 2022 18:23:05 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 May 2022 18:23:07 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:438a36bf0b6e75ff6f0fbb2b7669dfb86361416f4d808912d30cf5b91ad2eea9`  
		Last Modified: Wed, 11 May 2022 02:33:43 GMT  
		Size: 29.6 MB (29641051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff55daf61d8c0372d6e5e80fd8940594c5cf3e1352259087144ae34e2c1b914`  
		Last Modified: Wed, 25 May 2022 18:40:13 GMT  
		Size: 26.5 MB (26516231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c3d1f27084c9c2771e9986dc399ce44f90eeafa7ccdbd416915161f7861f6d`  
		Last Modified: Wed, 25 May 2022 18:39:57 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aef19cd7c9a944502a6d194b1ff6d69afec9b6ea545621097a72cb9275c2248`  
		Last Modified: Wed, 25 May 2022 18:39:58 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c9b049ad71bf536f23aa29ab8e75ac24f913ffcf50ee96e7574d5e12878582`  
		Last Modified: Wed, 25 May 2022 18:39:57 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4df5cc74404ca845810c40c15f24b1be92acffe993fff5a73ed2df13393484d`  
		Last Modified: Wed, 25 May 2022 18:39:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; ppc64le

```console
$ docker pull nginx@sha256:d536862048b7e508994a2de6660fb3276738e1eadbe44831927a9b05cca483a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64269534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e88ed42de7da005f552fc9db3cfcf4d19b9d37e5dc3892b4faea6a9f1b65a02a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 11 May 2022 01:32:29 GMT
ADD file:1e94716789ec21981460f74be38a668bc212bd804c1d41cecf90036a5bccac5a in / 
# Wed, 11 May 2022 01:32:34 GMT
CMD ["bash"]
# Wed, 11 May 2022 08:28:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 25 May 2022 18:17:51 GMT
ENV NGINX_VERSION=1.22.0
# Wed, 25 May 2022 18:17:56 GMT
ENV NJS_VERSION=0.7.4
# Wed, 25 May 2022 18:18:01 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 25 May 2022 18:36:34 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 25 May 2022 18:36:37 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Wed, 25 May 2022 18:36:38 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Wed, 25 May 2022 18:36:40 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Wed, 25 May 2022 18:36:41 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Wed, 25 May 2022 18:36:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 May 2022 18:36:51 GMT
EXPOSE 80
# Wed, 25 May 2022 18:36:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 May 2022 18:37:02 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2533109ed11eefd6415e0370d6d7a3ea879b582b1887c98b819a598ad18fca24`  
		Last Modified: Wed, 11 May 2022 01:43:03 GMT  
		Size: 35.3 MB (35286467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6915cd543a6065ba77da08c94cf48d849f0deb298335bed23376ca8ef656ac`  
		Last Modified: Wed, 25 May 2022 19:04:07 GMT  
		Size: 29.0 MB (28979504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2207a229b64a0f63ebb102683272695c12c56543c5629000fdc43d19a6821612`  
		Last Modified: Wed, 25 May 2022 19:04:02 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91c6602d2e2f680c1ce267ecfdf8e13278ed9749736cfdde2c01f18d3543412`  
		Last Modified: Wed, 25 May 2022 19:04:02 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434e54edb1c7664db15d32f1c085c9d7c1c08afdbd51d3bc3cd47a126b3c1eb9`  
		Last Modified: Wed, 25 May 2022 19:04:03 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2be20b9c1aac9966fff7db5a3393c59885c564b7c1cfe055794c5653f48dd0`  
		Last Modified: Wed, 25 May 2022 19:04:03 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; s390x

```console
$ docker pull nginx@sha256:9b3e0f8043185cdaa0795cf1bff8469ad5c6492f75e8482955c936075c4ffe31
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56211396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982d980996b2befef7e638fb31a3d9fe25e5d09ecbd059ad6360467cadd7fce3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 11 May 2022 00:44:17 GMT
ADD file:d93a1cf64a813d01774cd628dfd683c006e20159e2ab3464c2159c8d9897c725 in / 
# Wed, 11 May 2022 00:44:19 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:02:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 25 May 2022 17:42:27 GMT
ENV NGINX_VERSION=1.22.0
# Wed, 25 May 2022 17:42:28 GMT
ENV NJS_VERSION=0.7.4
# Wed, 25 May 2022 17:42:28 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 25 May 2022 17:45:53 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 25 May 2022 17:45:54 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Wed, 25 May 2022 17:45:54 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Wed, 25 May 2022 17:45:54 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Wed, 25 May 2022 17:45:54 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Wed, 25 May 2022 17:45:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 May 2022 17:45:55 GMT
EXPOSE 80
# Wed, 25 May 2022 17:45:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 May 2022 17:45:55 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9f3750f6094217808e26d471752341db88153c8d5b5f9bb11577b74671303bbc`  
		Last Modified: Wed, 11 May 2022 00:50:03 GMT  
		Size: 29.7 MB (29654739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0866308ea043b4ac99a47def338c1b1f9707a8386c4f4bb98f155277811b2a`  
		Last Modified: Wed, 25 May 2022 17:59:09 GMT  
		Size: 26.6 MB (26553100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c659e84e08b70d920956ec32ae2a827910871489929580a25c76da15fa2802c9`  
		Last Modified: Wed, 25 May 2022 17:59:06 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3869f17419838e04060a989f08dc3a79dd48baa8085db1056c9a497a53efec55`  
		Last Modified: Wed, 25 May 2022 17:59:05 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea8b4bb29983bbc2d06aa858591eaba54abb58c2850311f058c08db06d6edd4`  
		Last Modified: Wed, 25 May 2022 17:59:06 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab104072366fb9f83968f6efa893de83a7cde87b79535f8e8d02bd2916792c9`  
		Last Modified: Wed, 25 May 2022 17:59:06 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

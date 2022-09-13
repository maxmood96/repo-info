## `nginx:1-perl`

```console
$ docker pull nginx@sha256:70075a533f10611e0e0dccdf24fec77a8b2614d5f9b0e7f0462df5f82937e95d
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

### `nginx:1-perl` - linux; amd64

```console
$ docker pull nginx@sha256:36110bf21d938dead0bb1fe946ba7138b010d0e1772058abbb6429810664ece0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67928901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59849243daf9bf903302dd87571c1bf63e21a520ed0e01db8a032f78410ee488`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 03:58:43 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Aug 2022 03:58:43 GMT
ENV NGINX_VERSION=1.23.1
# Tue, 23 Aug 2022 03:58:43 GMT
ENV NJS_VERSION=0.7.6
# Tue, 23 Aug 2022 03:58:43 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 23 Aug 2022 03:59:26 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 23 Aug 2022 03:59:26 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 23 Aug 2022 03:59:26 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 23 Aug 2022 03:59:27 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 23 Aug 2022 03:59:27 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 23 Aug 2022 03:59:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 03:59:27 GMT
EXPOSE 80
# Tue, 23 Aug 2022 03:59:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Aug 2022 03:59:27 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0452e0853e08829c5125b27e70117b8b633fd5195b2789205436f86a6c95b36`  
		Last Modified: Tue, 23 Aug 2022 04:01:24 GMT  
		Size: 36.5 MB (36543864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ab0a967b65dab25a7a3e2764bdc20440869c428b57eb33e7164e08ca36e8d8`  
		Last Modified: Tue, 23 Aug 2022 04:01:18 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ca4910c020e4dff79a48cc931c59d47164957258bf8c4b458525e503ec9785`  
		Last Modified: Tue, 23 Aug 2022 04:01:18 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b1e8f3fe7163f4c62a27157dabc05919fbf6ba6829e5359fa2357bd2874416`  
		Last Modified: Tue, 23 Aug 2022 04:01:18 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8083621f433dc4c3b35056d5b760476bac2912519c80627807453711ef14ec`  
		Last Modified: Tue, 23 Aug 2022 04:01:18 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:d7eda1cde6a7b8d440e1b520931ab29fffe335883d2c2b944d36f25ef1434459
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63849851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8e74108461d23a5362df9a7e47f76454292296ad348ad1ab17b6ff9adabbb7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 13 Sep 2022 00:53:30 GMT
ADD file:539e23f1c3a625a612a5a59b3939e9692c86c3cfa4956d30f4802c9f34ffa29c in / 
# Tue, 13 Sep 2022 00:53:31 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:27:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Sep 2022 03:27:45 GMT
ENV NGINX_VERSION=1.23.1
# Tue, 13 Sep 2022 03:27:45 GMT
ENV NJS_VERSION=0.7.6
# Tue, 13 Sep 2022 03:27:45 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 13 Sep 2022 03:39:01 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 13 Sep 2022 03:39:01 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 13 Sep 2022 03:39:01 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 13 Sep 2022 03:39:01 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 13 Sep 2022 03:39:02 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 13 Sep 2022 03:39:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:39:02 GMT
EXPOSE 80
# Tue, 13 Sep 2022 03:39:02 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Sep 2022 03:39:02 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:705abbab4fcb3a8dfe046a2ae6c450328aa11d93911abce66d3bba8bc693cbd4`  
		Last Modified: Tue, 13 Sep 2022 01:01:07 GMT  
		Size: 28.9 MB (28905288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49d5af0622e674d3489e0c033d939e1a7534709e68707ffefb392164f8c2653`  
		Last Modified: Tue, 13 Sep 2022 03:48:06 GMT  
		Size: 34.9 MB (34941005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf082708d582cbcc398e29e7acf06c1cd118dc37fce7424420d01857e623b2c`  
		Last Modified: Tue, 13 Sep 2022 03:47:59 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01781a652113de9f7973aebf9c8901826b1262c8847af26a41851db091eb618`  
		Last Modified: Tue, 13 Sep 2022 03:47:59 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22225b45b4f8c00cd32d2fe02e8b0361df544a74ec1654fae7d5b68bda14b038`  
		Last Modified: Tue, 13 Sep 2022 03:47:59 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc1e79a9ab4f4f12ce47e1976e83e97278a79902b31d2a9263dc07cce24fb4d`  
		Last Modified: Tue, 13 Sep 2022 03:47:59 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:87aceef4230232630e27dccbe0bf3cb4574469c58dba43aab6ab2a1885d16f67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60488220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b27dde2483632a2992805db3b1045259dd58f81d36bbe18733419b831720de`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 23 Aug 2022 01:43:01 GMT
ADD file:4cd1b4287674228db28402a76aa4f241740585448be48b5b15068d275ee9eb84 in / 
# Tue, 23 Aug 2022 01:43:01 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 21:20:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Aug 2022 21:20:01 GMT
ENV NGINX_VERSION=1.23.1
# Tue, 23 Aug 2022 21:20:01 GMT
ENV NJS_VERSION=0.7.6
# Tue, 23 Aug 2022 21:20:01 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 23 Aug 2022 21:32:05 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 23 Aug 2022 21:32:05 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 23 Aug 2022 21:32:05 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 23 Aug 2022 21:32:05 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 23 Aug 2022 21:32:06 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 23 Aug 2022 21:32:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 21:32:06 GMT
EXPOSE 80
# Tue, 23 Aug 2022 21:32:06 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Aug 2022 21:32:06 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:051ba72559abd0cf65b34b75605580f58636ec3cb994f97de317632a85d82761`  
		Last Modified: Tue, 23 Aug 2022 01:50:05 GMT  
		Size: 26.6 MB (26571732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc299785e0ee84b982344bd3a60762ece66658bf239938d9a4c09b29b6f95350`  
		Last Modified: Tue, 23 Aug 2022 21:41:59 GMT  
		Size: 33.9 MB (33912925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc248d4f7ab92aa37918b98b00573a0885765871700878b3369438bdaddd3447`  
		Last Modified: Tue, 23 Aug 2022 21:41:50 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7910fa5a0b11645213d25b2c67c29298de7f067408c70a03d4bca1c6b053b20e`  
		Last Modified: Tue, 23 Aug 2022 21:41:49 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509f65bd81a3383b4e09e7a18872b8b9a68a9ecb69364bdab5d7b918711d4f7b`  
		Last Modified: Tue, 23 Aug 2022 21:41:49 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e5ac2231bbca0c1a261ca5e9f5575b2b210fb80e76eb76e5cc9a5125b80ad0`  
		Last Modified: Tue, 23 Aug 2022 21:41:49 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:2f28bdeb3cd13e557925ca58f482465c93d333ec3d2a4ffdc2c096e599bf974f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66443837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35057eb58fd2da0b624fa9d5efbc1d384d9802d6c74d0f614e9c0633345d0021`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:45:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Aug 2022 04:45:27 GMT
ENV NGINX_VERSION=1.23.1
# Tue, 23 Aug 2022 04:45:28 GMT
ENV NJS_VERSION=0.7.6
# Tue, 23 Aug 2022 04:45:29 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 23 Aug 2022 04:46:22 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 23 Aug 2022 04:46:24 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 23 Aug 2022 04:46:25 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 23 Aug 2022 04:46:26 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 23 Aug 2022 04:46:27 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 23 Aug 2022 04:46:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 04:46:28 GMT
EXPOSE 80
# Tue, 23 Aug 2022 04:46:29 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Aug 2022 04:46:30 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3071f167ff855ac73352e790596838c8e7237a2a04bd7d427db33e80c0de001`  
		Last Modified: Tue, 23 Aug 2022 04:49:31 GMT  
		Size: 36.4 MB (36376497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b88d84ca96126fc2b7e6cefac40d2e4a14f70bc35506b3ee6c8d4ea78dd035`  
		Last Modified: Tue, 23 Aug 2022 04:49:25 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a32741e2d8f64fa436238384f2f8a4aaed9b3e6f7558def89532131cdfeda16`  
		Last Modified: Tue, 23 Aug 2022 04:49:25 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bcfdfe4367f94eeceec085836b1b6bc5483046791ea4ae2381d9e03d06e762`  
		Last Modified: Tue, 23 Aug 2022 04:49:25 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467fe39d80b40f7e1d34ee143169e500e92667d2c8f0577b1d06bba03268446d`  
		Last Modified: Tue, 23 Aug 2022 04:49:25 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-perl` - linux; 386

```console
$ docker pull nginx@sha256:fa2c118a26385ef1ef278b6e115adc86750967f25236faea469ab67621ce20e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69337772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73e3eb6deac31bfccfb37069a6e16d126c8ebe9c0b522680c0dedf495d8742e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 23 Aug 2022 01:02:40 GMT
ADD file:5ca62c98116941aaa64ec72afb689a088c46f75a3e83d5b0d4e58d65ec905ccd in / 
# Tue, 23 Aug 2022 01:02:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 12:00:56 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Aug 2022 12:00:56 GMT
ENV NGINX_VERSION=1.23.1
# Tue, 23 Aug 2022 12:00:57 GMT
ENV NJS_VERSION=0.7.6
# Tue, 23 Aug 2022 12:00:58 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 23 Aug 2022 12:07:57 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 23 Aug 2022 12:07:58 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 23 Aug 2022 12:07:59 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 23 Aug 2022 12:08:00 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 23 Aug 2022 12:08:01 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 23 Aug 2022 12:08:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 12:08:02 GMT
EXPOSE 80
# Tue, 23 Aug 2022 12:08:03 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Aug 2022 12:08:04 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6b3cb4a05a891d9d8a87a2bd7247b16f79832a9d4afbad3ff5068f6fc2ba1560`  
		Last Modified: Tue, 23 Aug 2022 01:08:25 GMT  
		Size: 32.4 MB (32387317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad447c1fb7680348bbdaaf72c1d7498d612a292c50de9c370a095e8ecfad5d4`  
		Last Modified: Tue, 23 Aug 2022 12:15:03 GMT  
		Size: 36.9 MB (36946901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29000c736ebbc1dfd0fb0b4371ae37c6ab45ddf53f2bd7c5c886e3425b475d7`  
		Last Modified: Tue, 23 Aug 2022 12:14:56 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6708a6ac3b04dd7f3980edbe0eb80a32d3591e5c6a523487de2dba66c38478e6`  
		Last Modified: Tue, 23 Aug 2022 12:14:56 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b69c8fdf140f49262c2e238de1e03460b2ed9dfff7bbe223ec0d1ca2dad5c6`  
		Last Modified: Tue, 23 Aug 2022 12:14:56 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26c5c770238301748bdd26120a0a517a4cfce1a0111cccfcf63394bd795f37d`  
		Last Modified: Tue, 23 Aug 2022 12:14:56 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-perl` - linux; mips64le

```console
$ docker pull nginx@sha256:9d142ae7ffcba885e0d719e0e9753514dba73ea54d8b979f94712013a5cc02f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65345198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bb8e04131120fa407bf0d3c47763976a8d79bea396e7fdd0da7e3b6d466a8e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 23 Aug 2022 00:11:17 GMT
ADD file:37d58e8a76488fed0f1ebafd3ee993569a3c611b3a5d93400485783112b71386 in / 
# Tue, 23 Aug 2022 00:11:22 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:20:37 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Aug 2022 01:20:39 GMT
ENV NGINX_VERSION=1.23.1
# Tue, 23 Aug 2022 01:20:42 GMT
ENV NJS_VERSION=0.7.6
# Tue, 23 Aug 2022 01:20:44 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 23 Aug 2022 01:53:52 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 23 Aug 2022 01:53:55 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 23 Aug 2022 01:53:57 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 23 Aug 2022 01:54:00 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 23 Aug 2022 01:54:02 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 23 Aug 2022 01:54:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:54:08 GMT
EXPOSE 80
# Tue, 23 Aug 2022 01:54:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Aug 2022 01:54:14 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:0e8d4fbcc8d2fc93de0170727f6e48b6fc7ec8931443fbda8a8cd154dc6f7d36`  
		Last Modified: Tue, 23 Aug 2022 00:19:35 GMT  
		Size: 29.6 MB (29639012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf6ccadf87c32f295d2b643c6bf95ab3e9094eaf09bbfec7e969fb00c967127`  
		Last Modified: Tue, 23 Aug 2022 02:29:23 GMT  
		Size: 35.7 MB (35702625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4502604a6d2252df1db62fd36d95eaa9cd1a870fc0278f036800d1474015044e`  
		Last Modified: Tue, 23 Aug 2022 02:28:59 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2142980c181d32afecc2b12fb6f0915eddd258d11328d5c32b973ef770ddb99c`  
		Last Modified: Tue, 23 Aug 2022 02:28:59 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b346c72424987a25dad2ca47ecdf17c1e8711a5f37bdc40ed94d9810249033d`  
		Last Modified: Tue, 23 Aug 2022 02:28:59 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7dd2a0beaf155385d277868c76080d4072b327bd395103800308303d80d1efe`  
		Last Modified: Tue, 23 Aug 2022 02:28:59 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:01e0c16c2b0ed039d2280eb1eeef4c150a82020e25f13247649949eab60d7de8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73994192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59412b573ec47750f698ca9c52f0bd907a058fea14280f0283deee3c00f8926e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:30 GMT
ADD file:3a95a896d463569ce82199957052b3467123a4bd3385a0a4e397cf08402a99c3 in / 
# Tue, 02 Aug 2022 01:17:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:54:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 02 Aug 2022 03:54:35 GMT
ENV NGINX_VERSION=1.23.1
# Tue, 02 Aug 2022 03:54:35 GMT
ENV NJS_VERSION=0.7.6
# Tue, 02 Aug 2022 03:54:35 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 09 Aug 2022 18:59:49 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Aug 2022 18:59:51 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 09 Aug 2022 18:59:52 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 09 Aug 2022 18:59:52 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Aug 2022 18:59:52 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 09 Aug 2022 18:59:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:59:53 GMT
EXPOSE 80
# Tue, 09 Aug 2022 18:59:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 18:59:54 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5241cd116d6e6e2d62f3d8c2245b74daca9f6cc154eaccd738feb41984c74714`  
		Last Modified: Tue, 02 Aug 2022 01:24:39 GMT  
		Size: 35.3 MB (35272771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa7122365fca0824b12b84eaa41f2bf09dfa6463e82149cece56270bc7610cb`  
		Last Modified: Tue, 09 Aug 2022 19:32:14 GMT  
		Size: 38.7 MB (38717857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1d2b19495a4259feaffcd89effc1fce9f94fabd2d66b6726a0b348d77badd7`  
		Last Modified: Tue, 09 Aug 2022 19:32:04 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7073d5c2b3028b8ff5b78d16a813d406f130c7123f2ad236a0dad38a0f88518b`  
		Last Modified: Tue, 09 Aug 2022 19:32:04 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c13dcd53beec9d1aa1dad3e9bac02ee467782b217b9815a758a521057520d8`  
		Last Modified: Tue, 09 Aug 2022 19:32:04 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563deede0276c49824b060941cfae955e76f5f7ce0d8f9efdda7c3ede8c797b2`  
		Last Modified: Tue, 09 Aug 2022 19:32:04 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-perl` - linux; s390x

```console
$ docker pull nginx@sha256:7950daf1c19df80be9d9a3665012c6fd66179de9b6640ba346e4495bccd56bcd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66315517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec2cea6a1be3f2b9fbfdd0e16639b01eca6f37e08227eb708a445ef28db2cba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 13 Sep 2022 00:48:07 GMT
ADD file:e8a6c2e8be5d9d1f83c1e280419014489438391a9feb7c77b6c21adbf0ec062b in / 
# Tue, 13 Sep 2022 00:48:08 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:49:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Sep 2022 01:49:27 GMT
ENV NGINX_VERSION=1.23.1
# Tue, 13 Sep 2022 01:49:27 GMT
ENV NJS_VERSION=0.7.6
# Tue, 13 Sep 2022 01:49:27 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 13 Sep 2022 01:53:22 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 13 Sep 2022 01:53:24 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 13 Sep 2022 01:53:24 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 13 Sep 2022 01:53:24 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 13 Sep 2022 01:53:25 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 13 Sep 2022 01:53:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 01:53:25 GMT
EXPOSE 80
# Tue, 13 Sep 2022 01:53:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Sep 2022 01:53:25 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c64715e5ebd39975a39b5cf2535772544c27713cbed678b0a21e73680fffaf72`  
		Last Modified: Tue, 13 Sep 2022 00:52:39 GMT  
		Size: 29.6 MB (29635080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b2c975361d4a9bf5ba16d454b6ff570489d6d0cf26c8646a369b91deeb9caa`  
		Last Modified: Tue, 13 Sep 2022 01:58:29 GMT  
		Size: 36.7 MB (36676879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c035b0b660c5ca086f06ffaa9e0c36455b9c76f37c3686df53d08b2f85d5cfd`  
		Last Modified: Tue, 13 Sep 2022 01:58:24 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611ada6dff67e9551113a84f44d21a04afa7d981a6e1e095b75d16e8109e5119`  
		Last Modified: Tue, 13 Sep 2022 01:58:24 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b58b82862ff4101cd3d6bf0b5150439ab4017f7c04cac6c0e739cbc1ca8d9d`  
		Last Modified: Tue, 13 Sep 2022 01:58:24 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cad8311067727ae2ea37fbb7331bb896dde645d2cd3160cb79f7ef28849504`  
		Last Modified: Tue, 13 Sep 2022 01:58:24 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

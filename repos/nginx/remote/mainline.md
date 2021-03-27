## `nginx:mainline`

```console
$ docker pull nginx@sha256:e5e61af4e0cfcaf799d18aa422463f1c9770fee46f634abf51b74d33594ca338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `nginx:mainline` - linux; amd64

```console
$ docker pull nginx@sha256:48d56bae87c65ca642b0a1d13c3dc97c4430994991e5531ff123f77cdf975fae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53681790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6084105296a952523c36eea261af38885f41e9d1d0001b4916fa426e45377ffe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 12:33:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 12 Mar 2021 12:33:46 GMT
ENV NGINX_VERSION=1.19.8
# Fri, 12 Mar 2021 12:33:46 GMT
ENV NJS_VERSION=0.5.2
# Fri, 12 Mar 2021 12:33:46 GMT
ENV PKG_RELEASE=1~buster
# Fri, 12 Mar 2021 12:34:08 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 12 Mar 2021 12:34:08 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 12 Mar 2021 12:34:08 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 12 Mar 2021 12:34:09 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 12 Mar 2021 12:34:09 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 12 Mar 2021 12:34:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Mar 2021 12:34:09 GMT
EXPOSE 80
# Fri, 12 Mar 2021 12:34:10 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Mar 2021 12:34:10 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f7ebf60efda2064ed8f3ca5f748b757c9eb4194e8db766ee370067d2c72210`  
		Last Modified: Fri, 12 Mar 2021 12:36:37 GMT  
		Size: 26.6 MB (26577218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879a7c160ac652fea0b56d0d28a9fe5a4dfb9716fe0147c5d163a841c8d83fae`  
		Last Modified: Fri, 12 Mar 2021 12:36:32 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de58cd48a671f1121ff5cc9f04cb93916d1a71f25c378f3048975421d87f5a05`  
		Last Modified: Fri, 12 Mar 2021 12:36:31 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be704f37b5f442aeb0ee33e0a86d08263d23e7343321b4fc96b68d71e869e3b4`  
		Last Modified: Fri, 12 Mar 2021 12:36:31 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158aac73782cb5bf2f03cc3b3f9afa49ce582c26a546f6dba65994d1c7ddd43d`  
		Last Modified: Fri, 12 Mar 2021 12:36:31 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline` - linux; arm variant v5

```console
$ docker pull nginx@sha256:f6c9e4f5833764a47eb9b3e9dc5ce255c97e8aeafefc44ebb2fad21e5fb32b57
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50360370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2da10d4b169e4d59e82a1ee68c609ebef8b40ba493db9ffdfee3ca7a8abaa78`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 26 Mar 2021 07:51:46 GMT
ADD file:3dd25698bf1578e8580b2f437a2199bfc3b1818480b874d73622357e955a091f in / 
# Fri, 26 Mar 2021 07:51:48 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 09:44:37 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 26 Mar 2021 09:44:38 GMT
ENV NGINX_VERSION=1.19.8
# Fri, 26 Mar 2021 09:44:43 GMT
ENV NJS_VERSION=0.5.2
# Fri, 26 Mar 2021 09:44:44 GMT
ENV PKG_RELEASE=1~buster
# Fri, 26 Mar 2021 09:52:09 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 26 Mar 2021 09:52:12 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 26 Mar 2021 09:52:15 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 26 Mar 2021 09:52:18 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 26 Mar 2021 09:52:20 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 26 Mar 2021 09:52:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 09:52:25 GMT
EXPOSE 80
# Fri, 26 Mar 2021 09:52:27 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 09:52:31 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:997e59852ec0e1a23e4a179db14793947d60390c392ce15abc0f811e797c49ca`  
		Last Modified: Fri, 26 Mar 2021 08:00:22 GMT  
		Size: 24.8 MB (24846159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b88816ff2c44fc61f5441ae5783d90298a44d0aa64d6ef749d249181bbe316`  
		Last Modified: Fri, 26 Mar 2021 10:17:30 GMT  
		Size: 25.5 MB (25510639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb27cb71285d3c2ae18c2e970447097b9d0cecd40d771383426ecddaa42fd81`  
		Last Modified: Fri, 26 Mar 2021 10:17:26 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbaf6ceb504d8453599dece5c2036d657f20daee989045e2f38c8b44d4b97a8`  
		Last Modified: Fri, 26 Mar 2021 10:17:26 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae70c8b0e768b23a41826c54cf0e432925c14d084c5b78f54d5e2bf5b1340e9`  
		Last Modified: Fri, 26 Mar 2021 10:17:24 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f406e8ee9c068eafcf599630915ec8638040453e0256390e96a80a8c6db371`  
		Last Modified: Fri, 26 Mar 2021 10:17:25 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline` - linux; arm variant v7

```console
$ docker pull nginx@sha256:5ac6dbaf583a38bb0feda1d5bbe1fd9ab75f47a8493280fb2853ddfaa8071a03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47321300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f718772a0b3fd278567d92f0417549dfb43d6322d939536a433213143d18b80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 12 Mar 2021 02:00:12 GMT
ADD file:123da9848f87c8ed4c5122a104b8650564c09767725916f822def7b645a019f1 in / 
# Fri, 12 Mar 2021 02:00:14 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:56:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 12 Mar 2021 03:56:34 GMT
ENV NGINX_VERSION=1.19.8
# Fri, 12 Mar 2021 03:56:35 GMT
ENV NJS_VERSION=0.5.2
# Fri, 12 Mar 2021 03:56:36 GMT
ENV PKG_RELEASE=1~buster
# Fri, 12 Mar 2021 04:03:02 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 12 Mar 2021 04:03:06 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 12 Mar 2021 04:03:08 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 12 Mar 2021 04:03:09 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 12 Mar 2021 04:03:10 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 12 Mar 2021 04:03:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Mar 2021 04:03:12 GMT
EXPOSE 80
# Fri, 12 Mar 2021 04:03:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Mar 2021 04:03:15 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:e12d26f75fe8b7fd14712965ff5178762227d07d2151bb35fa21105ddfc4a14a`  
		Last Modified: Fri, 12 Mar 2021 02:10:28 GMT  
		Size: 22.7 MB (22709467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d398f223554ebbe6c0bc8380b254ca2aaf5389274973a993210e9c06ba8569bb`  
		Last Modified: Fri, 12 Mar 2021 04:24:50 GMT  
		Size: 24.6 MB (24608257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4d8ce9c3128a1d51cf9dc27fa4e685cb4c5cf6984aa8b2397e5c3f56b9686b`  
		Last Modified: Fri, 12 Mar 2021 04:24:43 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5517fa3ebac39e3638bc020c9d16265d76bdf65154df96c284927575e98bf9`  
		Last Modified: Fri, 12 Mar 2021 04:24:43 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf908022ef4b2de33d21a2a3ebc95b87820866a4c473cf1e693d4722d66210b`  
		Last Modified: Fri, 12 Mar 2021 04:24:43 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f10c9f42883435de4b88b9dba087d41984da0c9ca086d086ad999207c7ea69`  
		Last Modified: Fri, 12 Mar 2021 04:24:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:6ec7206b35a3382a0e1d5438320a05d9ae7509ce82dd631f3912c13a1d312078
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52235720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3169fe28086d8abf62c71036aa640b0053c110812c0c187442ed68510e8f85da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:53 GMT
ADD file:6130ddc0a939dd72c0614de4aa77de47aa16fe211274bacb31995aa1a0526164 in / 
# Fri, 12 Mar 2021 01:53:56 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 06:00:04 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 12 Mar 2021 06:00:05 GMT
ENV NGINX_VERSION=1.19.8
# Fri, 12 Mar 2021 06:00:06 GMT
ENV NJS_VERSION=0.5.2
# Fri, 12 Mar 2021 06:00:07 GMT
ENV PKG_RELEASE=1~buster
# Fri, 12 Mar 2021 06:00:52 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 12 Mar 2021 06:00:54 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 12 Mar 2021 06:00:55 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 12 Mar 2021 06:00:56 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 12 Mar 2021 06:00:57 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 12 Mar 2021 06:00:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Mar 2021 06:00:58 GMT
EXPOSE 80
# Fri, 12 Mar 2021 06:01:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Mar 2021 06:01:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:706ee5d0a6b53d9257cbea22d8409fb22c867ab3a001c65f6b8bfd37dace0e58`  
		Last Modified: Fri, 12 Mar 2021 02:01:39 GMT  
		Size: 25.9 MB (25856512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a567e5940f0e5abd5d1a1346f30d68eeab0c7fc57c53c7dd7eaff6fe2218765d`  
		Last Modified: Fri, 12 Mar 2021 06:05:43 GMT  
		Size: 26.4 MB (26375635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0fc9adab530e625c8b34700b7869f6ed4a07bc8b06d5f17c7add7eea1c6eb8`  
		Last Modified: Fri, 12 Mar 2021 06:05:37 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f341a39794819972ff2b06dd8cc419a590c80ce1d896c9c098b1d50dd5c53238`  
		Last Modified: Fri, 12 Mar 2021 06:05:37 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715e6a9ff87ab79ba59674122315a9de84392523c9db7fe2eabe354f65002649`  
		Last Modified: Fri, 12 Mar 2021 06:05:37 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fda24d8097fff4530ea3a7ab829b491ed460f9ff2e8de09c73be0722660481`  
		Last Modified: Fri, 12 Mar 2021 06:05:37 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline` - linux; 386

```console
$ docker pull nginx@sha256:5fb5e4bef6a2e326c924bea73b5671767b151800c06996a824be7eb37f400840
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55197119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4a64ecb611e76080cf70875a28aaf4d1f57c2971ec9b6315be2430383e3964`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 12 Mar 2021 01:44:27 GMT
ADD file:90c103e04bd6fe0f39733cbf8eb2d8845aed3e4fc3fd1e5c3354df69e40aa615 in / 
# Fri, 12 Mar 2021 01:44:28 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 13:41:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 12 Mar 2021 13:41:35 GMT
ENV NGINX_VERSION=1.19.8
# Fri, 12 Mar 2021 13:41:35 GMT
ENV NJS_VERSION=0.5.2
# Fri, 12 Mar 2021 13:41:36 GMT
ENV PKG_RELEASE=1~buster
# Fri, 12 Mar 2021 13:41:58 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 12 Mar 2021 13:41:58 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 12 Mar 2021 13:41:58 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 12 Mar 2021 13:41:58 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 12 Mar 2021 13:41:59 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 12 Mar 2021 13:41:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Mar 2021 13:41:59 GMT
EXPOSE 80
# Fri, 12 Mar 2021 13:41:59 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Mar 2021 13:41:59 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:0898aa7472f57f223652846337cf862f142e109d0c039b41886e7f20c345f85e`  
		Last Modified: Fri, 12 Mar 2021 01:52:08 GMT  
		Size: 27.8 MB (27760948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b5216f71848e59fca510633b61dcd8bd6680d7cb5a3e2936812cb46ebbd55b`  
		Last Modified: Fri, 12 Mar 2021 13:45:19 GMT  
		Size: 27.4 MB (27432600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff5c6ce1e082c4240c37f21693bed56d7014657db952b72b0c2c9532397406f`  
		Last Modified: Fri, 12 Mar 2021 13:45:15 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460ebacc3fb9ff577f50ef935bf1a06b75eea71a2e58bcb846bd9b6335eddbbe`  
		Last Modified: Fri, 12 Mar 2021 13:45:13 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a332f1fc2b81811957a658dde9dabf4d3f7fa666fba98266f22eca0289bfc85`  
		Last Modified: Fri, 12 Mar 2021 13:45:14 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30fe0f7e8e3220f661bf85d744fdebaec45a8b0690c63a7c21124c0f361f3cf9`  
		Last Modified: Fri, 12 Mar 2021 13:45:13 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline` - linux; mips64le

```console
$ docker pull nginx@sha256:0a564e80a3156f2cc825d1720f303d59bd521da19bcbd01316870e1313ecbd23
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51910814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5508a64498e870412ec6b6dbd1675cd632afbde30347a9bab94bf52399797df8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 26 Mar 2021 08:09:56 GMT
ADD file:74d504a9a34f47729165ef4ceedc9f0eaa2e91bfb6a24ebfc3ceed0248267a27 in / 
# Fri, 26 Mar 2021 08:09:57 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 11:09:32 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 26 Mar 2021 11:09:33 GMT
ENV NGINX_VERSION=1.19.8
# Fri, 26 Mar 2021 11:09:33 GMT
ENV NJS_VERSION=0.5.2
# Fri, 26 Mar 2021 11:09:33 GMT
ENV PKG_RELEASE=1~buster
# Fri, 26 Mar 2021 11:21:13 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 26 Mar 2021 11:21:14 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 26 Mar 2021 11:21:14 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 26 Mar 2021 11:21:15 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 26 Mar 2021 11:21:15 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 26 Mar 2021 11:21:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 11:21:16 GMT
EXPOSE 80
# Fri, 26 Mar 2021 11:21:16 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 11:21:16 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5f863e006c40853ec8c23aa5b7a0e95918001f96878fb45770410ac4df51cf88`  
		Last Modified: Fri, 26 Mar 2021 08:16:29 GMT  
		Size: 25.8 MB (25772487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0902e30fda6dda945e2157133d51227e728cf1216e982e09d6a83d44d0e8ae`  
		Last Modified: Fri, 26 Mar 2021 11:58:18 GMT  
		Size: 26.1 MB (26134750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f47091a06e508634f6f09601c2496f720a3ac69c28ab489e35b3a40870c59e`  
		Last Modified: Fri, 26 Mar 2021 11:58:02 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdf8845b1659b8caeea45c2168111ce6587acf606d446d1a0aa7b8058f068c0`  
		Last Modified: Fri, 26 Mar 2021 11:58:02 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee450e92750d8c22a6fbeab2e061fd88c2b9b0b849bb4e3576f849aa73c7d4d2`  
		Last Modified: Fri, 26 Mar 2021 11:58:02 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750c7a359172d821fa5c515f39af7aa1b1a6b2f923b66cc32d4855997f71e72f`  
		Last Modified: Fri, 26 Mar 2021 11:58:02 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline` - linux; ppc64le

```console
$ docker pull nginx@sha256:3a9f0b1c80284e8979a43a042512e45742114c113985b5877fcc3b7ff2b1b65b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59172916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088791dee5b4ef9efadfded0261f55d0b6b9029f5c120adba178d7a317d1b86e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 12 Mar 2021 02:32:43 GMT
ADD file:6a0c0cfa71979cf6fdd859dce1e32582f0e55ed382b9e17b77a2001defc2c9db in / 
# Fri, 12 Mar 2021 02:32:50 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 06:40:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 12 Mar 2021 06:40:26 GMT
ENV NGINX_VERSION=1.19.8
# Fri, 12 Mar 2021 06:40:33 GMT
ENV NJS_VERSION=0.5.2
# Fri, 12 Mar 2021 06:40:43 GMT
ENV PKG_RELEASE=1~buster
# Fri, 12 Mar 2021 07:00:21 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 12 Mar 2021 07:00:24 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 12 Mar 2021 07:00:27 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 12 Mar 2021 07:00:28 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 12 Mar 2021 07:00:30 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 12 Mar 2021 07:00:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Mar 2021 07:00:36 GMT
EXPOSE 80
# Fri, 12 Mar 2021 07:00:39 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Mar 2021 07:00:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:1d686056fdac1848f4fd78ba2b335502055ffe98c79619e21d0c2fb7db95257e`  
		Last Modified: Fri, 12 Mar 2021 02:45:35 GMT  
		Size: 30.5 MB (30525728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2974c37dbc0ebf4354726642a7e0d4a581018fdba3b27bab923f81a35e0d255e`  
		Last Modified: Fri, 12 Mar 2021 08:20:10 GMT  
		Size: 28.6 MB (28643611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af93cd2107595fbfef81fb5aeb05cc98207f40801e31a39d2c440da60de927ec`  
		Last Modified: Fri, 12 Mar 2021 08:20:05 GMT  
		Size: 599.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c669516ef60f35f99a3df6e4f4852ebbc7aad0496936b34de16300b93cf87963`  
		Last Modified: Fri, 12 Mar 2021 08:20:05 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b026b649f22698a28e7c2af59014b0472633d3f373fe58918b94c5b9c205b64`  
		Last Modified: Fri, 12 Mar 2021 08:20:04 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578540f287f5bf9c6982d8684b9ea6f6e0fa38392ba40a6afb01c2066a548763`  
		Last Modified: Fri, 12 Mar 2021 08:20:04 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline` - linux; s390x

```console
$ docker pull nginx@sha256:af0ac023b3643d881a41be070818c5aa9e8cc0b7510ce5e568a990048ce991d9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51875981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e7b7f537f759c642b254b5d931c35ed1b9d8e1ce6c97b42337727eb4171157`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 26 Mar 2021 10:53:48 GMT
ADD file:3a3cf2e796c665cae881fb0b8a23a071206531af98c03548ab5a8721b3c67353 in / 
# Fri, 26 Mar 2021 10:53:49 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 16:16:14 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 26 Mar 2021 16:16:15 GMT
ENV NGINX_VERSION=1.19.8
# Fri, 26 Mar 2021 16:16:15 GMT
ENV NJS_VERSION=0.5.2
# Fri, 26 Mar 2021 16:16:16 GMT
ENV PKG_RELEASE=1~buster
# Fri, 26 Mar 2021 16:22:12 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 26 Mar 2021 16:22:15 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 26 Mar 2021 16:22:16 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 26 Mar 2021 16:22:16 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 26 Mar 2021 16:22:17 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 26 Mar 2021 16:22:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 16:22:18 GMT
EXPOSE 80
# Fri, 26 Mar 2021 16:22:19 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 16:22:19 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a37ca8d63090f0f22441ceecc0af7881a2668336202cf586e841e3d9e06f2f4b`  
		Last Modified: Fri, 26 Mar 2021 10:57:46 GMT  
		Size: 25.7 MB (25716264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13b5a5c3e2486793553ac872cd6dc836ea27d462f2ff1819c54d77700676302`  
		Last Modified: Fri, 26 Mar 2021 16:42:16 GMT  
		Size: 26.2 MB (26156142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f364738b089f1abe3267f7f7189d7cb18f9cab0798135b02c206c7c66303982`  
		Last Modified: Fri, 26 Mar 2021 16:42:11 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c31a6e4749cfb0ec1a4516b903a1ec842d13923ce684c8cfcb4aa38a77d79`  
		Last Modified: Fri, 26 Mar 2021 16:42:11 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9001c4f82b9464b2845916f815dc6c4e5cc36c9ff990903eb266eed68532dba4`  
		Last Modified: Fri, 26 Mar 2021 16:42:11 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ec33af7fcd6fc94851b6b911ce576d499a7927247b5821485ad8da8de27ca4`  
		Last Modified: Fri, 26 Mar 2021 16:42:11 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

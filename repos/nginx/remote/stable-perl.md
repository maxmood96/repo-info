## `nginx:stable-perl`

```console
$ docker pull nginx@sha256:d4c39412b7cca4f1193b3c6ffb64b3525bf19d8107d82ba5f950d3cc0da3ba19
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

### `nginx:stable-perl` - linux; amd64

```console
$ docker pull nginx@sha256:1cfac6bf8a435d23049021ce3e76da683a3d1c43fe55050bb34eb38748a78bad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64676199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7b0be24eed476c991874394fa387ee984c526f68268763e2875505399371ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:03:10 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 12 Oct 2021 02:04:21 GMT
ENV NGINX_VERSION=1.20.1
# Tue, 12 Oct 2021 02:04:21 GMT
ENV NJS_VERSION=0.5.3
# Tue, 12 Oct 2021 02:04:21 GMT
ENV PKG_RELEASE=1~buster
# Tue, 12 Oct 2021 02:05:14 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 12 Oct 2021 02:05:15 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 12 Oct 2021 02:05:15 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 12 Oct 2021 02:05:15 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 02:05:15 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 12 Oct 2021 02:05:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 02:05:16 GMT
EXPOSE 80
# Tue, 12 Oct 2021 02:05:16 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Oct 2021 02:05:16 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed628001eed34161794c452a02805ab3845ee492a62ea3c581aeaa3eae1af685`  
		Last Modified: Tue, 12 Oct 2021 02:07:11 GMT  
		Size: 37.5 MB (37533142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817211fec02631968ec81762ea1349c1e90ce92f0b95ffa759964bc7b3000ad0`  
		Last Modified: Tue, 12 Oct 2021 02:07:05 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f2099533cd2e254e6975d94959710c3285f8d573a443e66f634b27d4263b33`  
		Last Modified: Tue, 12 Oct 2021 02:07:05 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3f41dff7d220fb9c1d47d21eb6079626b11f1addc52782d0144f96022af104`  
		Last Modified: Tue, 12 Oct 2021 02:07:05 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9097ac386706e3c49e62b0dc72e626ba4bcbab2c1894b7b75158baf315cdc81b`  
		Last Modified: Tue, 12 Oct 2021 02:07:05 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:97b26b3ee460668a6b066bf0f2d5c5f7005977f0411cfc52a8a10da9c7d1cfca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60603920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d31831ce62499a04dee62e4c9b20cfe89ccf42cb51f8dba62003d54e519676d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 03:38:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 28 Sep 2021 03:57:40 GMT
ENV NGINX_VERSION=1.20.1
# Tue, 28 Sep 2021 03:57:40 GMT
ENV NJS_VERSION=0.5.3
# Tue, 28 Sep 2021 03:57:41 GMT
ENV PKG_RELEASE=1~buster
# Tue, 28 Sep 2021 04:16:32 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 28 Sep 2021 04:16:32 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 28 Sep 2021 04:16:33 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 28 Sep 2021 04:16:33 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 28 Sep 2021 04:16:34 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 28 Sep 2021 04:16:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 04:16:35 GMT
EXPOSE 80
# Tue, 28 Sep 2021 04:16:35 GMT
STOPSIGNAL SIGQUIT
# Tue, 28 Sep 2021 04:16:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6d3e5487645fb79a6fd219ae3bfeee3447402ae2762dd1398a25b130718794`  
		Last Modified: Tue, 28 Sep 2021 04:20:42 GMT  
		Size: 35.7 MB (35721293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf76af8e0503b559a25ded676750ea6dcdf4d690ad230ab67e58ac981c54b234`  
		Last Modified: Tue, 28 Sep 2021 04:20:19 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8563b3682d3a3cd2dc34925dff217a1adc85dd66da18e66084b739b7d40eb07`  
		Last Modified: Tue, 28 Sep 2021 04:20:19 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167dfd9866259ed051032461682ea3b2a10200469112083fb3341fae5f4d8a28`  
		Last Modified: Tue, 28 Sep 2021 04:20:19 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2e90365f549c0ec60d284548c4fc0fceee9ec0d2b5d466c5e491139bfd205e`  
		Last Modified: Tue, 28 Sep 2021 04:20:19 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:5eb9c4584a33240230f72ef2b9b1a32b35ea95dd78e4244c0fd28f7de038e9e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57361247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c569481c37231a5de9819a83786e80607465644a6cadcd09b38698a3ddecadcf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 30 Sep 2021 18:04:11 GMT
ADD file:e71f315aa894d483f75b32109fff32974c43ce2e684cd28eb6492bc6fc450931 in / 
# Thu, 30 Sep 2021 18:04:12 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 06:27:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 01 Oct 2021 06:46:06 GMT
ENV NGINX_VERSION=1.20.1
# Fri, 01 Oct 2021 06:46:06 GMT
ENV NJS_VERSION=0.5.3
# Fri, 01 Oct 2021 06:46:07 GMT
ENV PKG_RELEASE=1~buster
# Fri, 01 Oct 2021 07:03:48 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 01 Oct 2021 07:03:49 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 01 Oct 2021 07:03:49 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 01 Oct 2021 07:03:50 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 01 Oct 2021 07:03:50 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Fri, 01 Oct 2021 07:03:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Oct 2021 07:03:51 GMT
EXPOSE 80
# Fri, 01 Oct 2021 07:03:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Oct 2021 07:03:52 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:421f17c521234da0c5b07d4f6e44314149dc3790ef12134e85e61741452c9f96`  
		Last Modified: Thu, 30 Sep 2021 18:20:50 GMT  
		Size: 22.7 MB (22746246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce5ce4aced8fb2342043e015d9c0ead3b885bc2b92a42d35f68409529f676ff`  
		Last Modified: Fri, 01 Oct 2021 07:09:12 GMT  
		Size: 34.6 MB (34611439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b727db8ab5c034a81b52034e9c5e1e20741db9aa84bcc8d42faabad46c128d`  
		Last Modified: Fri, 01 Oct 2021 07:08:49 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab7d0513bcce302ef60ff665db66d80c28103eb5c6cd42c718d6c4b6bfb3339`  
		Last Modified: Fri, 01 Oct 2021 07:08:49 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63634658a91ce410d438c672199e7abb050c8ff4f1a37eb49d867997ffe8795`  
		Last Modified: Fri, 01 Oct 2021 07:08:49 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c2ebfb6710e4c2ca51880c9e9ae92bfd2168e6aed63ce055f7b18d58a29ca7`  
		Last Modified: Fri, 01 Oct 2021 07:08:49 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:add50b2b3a591d473c50bf9a026c451a90f58ee0df0e55975faba38566e709d4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63172028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3ab2a7a3c8037a529a69b65afeba0bbd348013583dfa9ded4051f3b4bc4c7e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 05:35:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 28 Sep 2021 05:37:02 GMT
ENV NGINX_VERSION=1.20.1
# Tue, 28 Sep 2021 05:37:02 GMT
ENV NJS_VERSION=0.5.3
# Tue, 28 Sep 2021 05:37:02 GMT
ENV PKG_RELEASE=1~buster
# Tue, 28 Sep 2021 05:38:08 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 28 Sep 2021 05:38:09 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 28 Sep 2021 05:38:09 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 28 Sep 2021 05:38:09 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 28 Sep 2021 05:38:09 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 28 Sep 2021 05:38:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 05:38:10 GMT
EXPOSE 80
# Tue, 28 Sep 2021 05:38:10 GMT
STOPSIGNAL SIGQUIT
# Tue, 28 Sep 2021 05:38:10 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1188f2c58b6e78a18928973a1528f457cf1731b79d88e69716bc35690e0f9b`  
		Last Modified: Tue, 28 Sep 2021 05:41:03 GMT  
		Size: 37.3 MB (37253434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aca25f53fdc4a493e439bab520b566aa63ef537ca306f9cc6bce4726787c482`  
		Last Modified: Tue, 28 Sep 2021 05:40:57 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44e1503e6a53ed68c7c3e2d164ff5a481a6bae83a8c4c8f17b55a45166ddf01`  
		Last Modified: Tue, 28 Sep 2021 05:40:57 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4961a46f332ef511d5157741f0f59dd83e4a2da9805997fa50497900f2435f`  
		Last Modified: Tue, 28 Sep 2021 05:40:57 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b19d89f19178d3afc7311a1d0f03df5ab6e6992e1d656693236908b022f45e5`  
		Last Modified: Tue, 28 Sep 2021 05:40:57 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; 386

```console
$ docker pull nginx@sha256:bfc194e66bc39085efba04c5c6a8bd5c1dfa24d30a42ae8dbc2cde97fdcaa58c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65656473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39836dc4253db7c02f33cdfd3f8597325d335c15fc827acf2bbe30c8c3b75028`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:36:39 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 28 Sep 2021 08:38:23 GMT
ENV NGINX_VERSION=1.20.1
# Tue, 28 Sep 2021 08:38:24 GMT
ENV NJS_VERSION=0.5.3
# Tue, 28 Sep 2021 08:38:24 GMT
ENV PKG_RELEASE=1~buster
# Tue, 28 Sep 2021 08:39:26 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 28 Sep 2021 08:39:27 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 28 Sep 2021 08:39:27 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 28 Sep 2021 08:39:27 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 28 Sep 2021 08:39:27 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 28 Sep 2021 08:39:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 08:39:28 GMT
EXPOSE 80
# Tue, 28 Sep 2021 08:39:28 GMT
STOPSIGNAL SIGQUIT
# Tue, 28 Sep 2021 08:39:28 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41ca29dfe8f55d7e43b56fbda9e4390425cf460226dcff8b60b6e07f198ae41`  
		Last Modified: Tue, 28 Sep 2021 08:42:01 GMT  
		Size: 37.9 MB (37855288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee85f16a8e41430728e1e33fe6cef504c5a8c6fec31b48050a1092aee91961a5`  
		Last Modified: Tue, 28 Sep 2021 08:41:52 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f2551861301d637bf9fcfef04ec40d5e752edfc1a9d5f3cfeaa82c365dfa5f`  
		Last Modified: Tue, 28 Sep 2021 08:41:52 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4604647fc67ad321870f399d64ab759a71b06048c7e350e1d6818402b52a034`  
		Last Modified: Tue, 28 Sep 2021 08:41:53 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f62998a438fce38db9678a4fd6637a670cabd8344b13caa9ebdeaada5e7872d`  
		Last Modified: Tue, 28 Sep 2021 08:41:52 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; mips64le

```console
$ docker pull nginx@sha256:25c44a2d5f1813a3d95a7614b8fc4569fe42fd85404fd4d5ded765e1cee3f35a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62169273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fdb558d8db1b76ac84f3e55b0768bbab63b5a8ba854851f173527385167c8da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 03 Sep 2021 01:10:49 GMT
ADD file:219b2ce847fd4b227257f60cf40dee2eaf7688371fd76658752f6ccbac9c4353 in / 
# Fri, 03 Sep 2021 01:10:49 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:40:19 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 Sep 2021 03:05:18 GMT
ENV NGINX_VERSION=1.20.1
# Fri, 03 Sep 2021 03:05:19 GMT
ENV NJS_VERSION=0.5.3
# Fri, 03 Sep 2021 03:05:19 GMT
ENV PKG_RELEASE=1~buster
# Fri, 03 Sep 2021 03:29:38 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 03 Sep 2021 03:29:39 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 03 Sep 2021 03:29:40 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 03 Sep 2021 03:29:40 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 03 Sep 2021 03:29:41 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Fri, 03 Sep 2021 03:29:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 Sep 2021 03:29:41 GMT
EXPOSE 80
# Fri, 03 Sep 2021 03:29:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 03 Sep 2021 03:29:42 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c11f388d181c313e7657eea7b1ffa2d20856b4701922412adea724a19acdb79f`  
		Last Modified: Fri, 03 Sep 2021 01:19:51 GMT  
		Size: 25.8 MB (25812853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae3cfaeea6251141a520dac0649b0c1f72b5c7aee78036ac1ab155b60a7dcc7`  
		Last Modified: Fri, 03 Sep 2021 03:32:18 GMT  
		Size: 36.4 MB (36352857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebeceabf601bfd61da8b23d377b6153f6939860ed7a537062f6b08c7d8a3406e`  
		Last Modified: Fri, 03 Sep 2021 03:31:52 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dcd22174cf8c8aca6ef6e9d174e7e2f7b72f8d9541c69209e1ace5385abed1`  
		Last Modified: Fri, 03 Sep 2021 03:31:52 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d2a2ea78058d58f9873cbdaa26206599cabad4c425f34a4e65090ae5e0afa8`  
		Last Modified: Fri, 03 Sep 2021 03:31:52 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde816196961dbb389e2ed9932c2eb6a5a6742068ec1d51799f4211826936074`  
		Last Modified: Fri, 03 Sep 2021 03:31:52 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:82f5e5487093dc9087e26eb3b3c70618ec5b54c302bb87eb3a442aac634b0c31
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70395047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c2d3e96c94fc5521920b8c755e74a2f9ecbc0a4b967ff7fad583100a0dbf5c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 04 Oct 2021 17:56:14 GMT
ADD file:0b55ec14c2e9aa78512985a5bff3881b6fabf6794ce4406bb874b173d5a60799 in / 
# Mon, 04 Oct 2021 17:56:20 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 16:30:18 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 05 Oct 2021 17:10:47 GMT
ENV NGINX_VERSION=1.20.1
# Tue, 05 Oct 2021 17:10:51 GMT
ENV NJS_VERSION=0.5.3
# Tue, 05 Oct 2021 17:10:54 GMT
ENV PKG_RELEASE=1~buster
# Tue, 05 Oct 2021 17:41:35 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 05 Oct 2021 17:41:42 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 05 Oct 2021 17:41:44 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 05 Oct 2021 17:41:45 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 05 Oct 2021 17:41:46 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 05 Oct 2021 17:41:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:41:53 GMT
EXPOSE 80
# Tue, 05 Oct 2021 17:41:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Oct 2021 17:41:59 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5736db2c6d2424206be3309412da520d7fe1fe4933cc2cc72641b311dd7d9099`  
		Last Modified: Mon, 04 Oct 2021 18:08:33 GMT  
		Size: 30.6 MB (30553728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babf089edf2d83093912bd64dcead845c11e2aacd5792fd56496ad8df6e9a500`  
		Last Modified: Tue, 05 Oct 2021 17:44:45 GMT  
		Size: 39.8 MB (39837763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4ec870da97cc9fd66cdf13d74bb4321af0db7c74a7b2683fe9884c06c22ee4`  
		Last Modified: Tue, 05 Oct 2021 17:44:37 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3486025e2e10b4a044b760784482eb73d6474dccddfb0db8aeb26c5186cd921`  
		Last Modified: Tue, 05 Oct 2021 17:44:37 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdb87def5adcf3882d42efb74b65cacd375b3ed78bfc5635893783d2336f6d9`  
		Last Modified: Tue, 05 Oct 2021 17:44:37 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5960b089b9af291f65fc967563b4197bafb0b7210aa721249a0de0bb07b12b`  
		Last Modified: Tue, 05 Oct 2021 17:44:37 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-perl` - linux; s390x

```console
$ docker pull nginx@sha256:b6c1c9a773484f2f49cc8c95d09910605c2715869302596d474a13594113f0ed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63151407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbfb33aac4bfdc7781ba98bc488dcc1d1c43455bedd54ff29572fd004e5364a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 28 Sep 2021 01:43:29 GMT
ADD file:118e7a596407435b5e2ff0aae6bb9bff3b66000c91ca37bfe1eeb98c23d99d49 in / 
# Tue, 28 Sep 2021 01:43:30 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 05:29:56 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 28 Sep 2021 05:35:32 GMT
ENV NGINX_VERSION=1.20.1
# Tue, 28 Sep 2021 05:35:32 GMT
ENV NJS_VERSION=0.5.3
# Tue, 28 Sep 2021 05:35:32 GMT
ENV PKG_RELEASE=1~buster
# Tue, 28 Sep 2021 05:40:16 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 28 Sep 2021 05:40:18 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 28 Sep 2021 05:40:18 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 28 Sep 2021 05:40:18 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 28 Sep 2021 05:40:18 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 28 Sep 2021 05:40:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 05:40:19 GMT
EXPOSE 80
# Tue, 28 Sep 2021 05:40:19 GMT
STOPSIGNAL SIGQUIT
# Tue, 28 Sep 2021 05:40:19 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7cfe208f95c1b63305981b069795676fa149e7115b9044c241ee45ef4aaf0bb3`  
		Last Modified: Tue, 28 Sep 2021 01:49:36 GMT  
		Size: 25.8 MB (25760871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0525414e2a4393bed9edfd9972f46da2816fbf644e40c1032ed4c076643e956f`  
		Last Modified: Tue, 28 Sep 2021 05:42:36 GMT  
		Size: 37.4 MB (37386977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c9f7d70dad3f4b0f89d06bd77e0156c4f3660aaa99c3f883b5635bfd848c7a`  
		Last Modified: Tue, 28 Sep 2021 05:42:31 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d88e405ccf93c0307f31c8d905f7578c55313c30eaa24abb6d731d3b30fd0ce`  
		Last Modified: Tue, 28 Sep 2021 05:42:31 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d660d706ee2d84c08749a14e59f254b80891e079f81b95099d8c71d57e9ad22`  
		Last Modified: Tue, 28 Sep 2021 05:42:31 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820bef0474bf44266fea886237382ad362d4c1bc4d78e78defb97179c2924957`  
		Last Modified: Tue, 28 Sep 2021 05:42:31 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nginx:stable`

```console
$ docker pull nginx@sha256:b05750bf8835edcab35b144006d420970188c1597048ba60935c32abd6e0b5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `nginx:stable` - linux; amd64

```console
$ docker pull nginx@sha256:70284e939ab66440d71fd30df4188ba9be4a4f6aec18d6edf20f729103ca1b5c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50970433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960143eb89651560fcc96fd6b36c4f9f6470bbd8e74bd5b53d0009066b1e9606`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 15:19:56 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Sat, 28 Dec 2019 15:21:18 GMT
ENV NGINX_VERSION=1.16.1
# Wed, 22 Jan 2020 04:27:56 GMT
ENV NJS_VERSION=0.3.8
# Wed, 22 Jan 2020 04:27:56 GMT
ENV PKG_RELEASE=1~buster
# Wed, 22 Jan 2020 04:28:27 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base     && apt-get remove --purge --auto-remove -y ca-certificates && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi
# Wed, 22 Jan 2020 04:28:28 GMT
RUN ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log
# Wed, 22 Jan 2020 04:28:28 GMT
EXPOSE 80
# Wed, 22 Jan 2020 04:28:29 GMT
STOPSIGNAL SIGTERM
# Wed, 22 Jan 2020 04:28:29 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6415272b82847f3c2cc20b19ca37c242a483845fc4d3aa1b1eba77c781db3220`  
		Last Modified: Wed, 22 Jan 2020 04:31:01 GMT  
		Size: 23.9 MB (23877954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eefdcfe0c520576f6e0c53d0b81398e6030a36d9ad3d88c1b6eda5b4fa9a866`  
		Last Modified: Wed, 22 Jan 2020 04:30:55 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; arm variant v7

```console
$ docker pull nginx@sha256:90873c5b404db3e97e0f24660c649c4be7144d9163b66486303c3f06a2ccce59
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44932051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8021ea91a23b568259d671c34605af452be88d1ef90f48583659e6f40f8e79bc`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 28 Dec 2019 04:59:06 GMT
ADD file:d252ae1c97d5c80e71e64a51cc4d137a901e0e6cdc4aec29faa917fa9bcf3242 in / 
# Sat, 28 Dec 2019 04:59:08 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 12:15:56 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Sat, 28 Dec 2019 12:29:23 GMT
ENV NGINX_VERSION=1.16.1
# Wed, 22 Jan 2020 02:32:17 GMT
ENV NJS_VERSION=0.3.8
# Wed, 22 Jan 2020 02:32:18 GMT
ENV PKG_RELEASE=1~buster
# Wed, 22 Jan 2020 02:38:01 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base     && apt-get remove --purge --auto-remove -y ca-certificates && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi
# Wed, 22 Jan 2020 02:38:06 GMT
RUN ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log
# Wed, 22 Jan 2020 02:38:07 GMT
EXPOSE 80
# Wed, 22 Jan 2020 02:38:08 GMT
STOPSIGNAL SIGTERM
# Wed, 22 Jan 2020 02:38:09 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c4f8e1e649d2e7938fbe832f157cfb695319ee625a8bc06c619219a87d550949`  
		Last Modified: Sat, 28 Dec 2019 05:07:32 GMT  
		Size: 22.7 MB (22699129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f323561d5b41e79094a531345020c039f3fc48d122312568a175e4f35549e647`  
		Last Modified: Wed, 22 Jan 2020 02:46:53 GMT  
		Size: 22.2 MB (22232717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dbe4ef9aee68e58f5eb56cc0b4a995167a70ec925a53395c2686496f077642`  
		Last Modified: Wed, 22 Jan 2020 02:46:45 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:0480edb9c8b498ad51c3885f4e9c517d1560c992e0c3c0669b101a99cc0ba697
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49668229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1341289458840a569945db3736e3e2dbf9d5bacb0ea98f2c50960e03e075332`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:08 GMT
ADD file:b45fd612576b682e93ab91addbc4387a6609ace4bc092e5b615323964bba33c3 in / 
# Sat, 28 Dec 2019 04:41:11 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:56:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Sat, 28 Dec 2019 09:10:32 GMT
ENV NGINX_VERSION=1.16.1
# Wed, 22 Jan 2020 03:28:08 GMT
ENV NJS_VERSION=0.3.8
# Wed, 22 Jan 2020 03:28:09 GMT
ENV PKG_RELEASE=1~buster
# Wed, 22 Jan 2020 03:33:44 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base     && apt-get remove --purge --auto-remove -y ca-certificates && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi
# Wed, 22 Jan 2020 03:33:47 GMT
RUN ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log
# Wed, 22 Jan 2020 03:33:47 GMT
EXPOSE 80
# Wed, 22 Jan 2020 03:33:48 GMT
STOPSIGNAL SIGTERM
# Wed, 22 Jan 2020 03:33:48 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:fb62b7c746da1f79992359282f2d8b7f93da8c48dc138ec6b2a36130efd42635`  
		Last Modified: Sat, 28 Dec 2019 04:46:58 GMT  
		Size: 25.9 MB (25850702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50219c10a38e2f15f22b87a8fb06dcf4b7ca754b70e0e86564f459a8ea1a0c6`  
		Last Modified: Wed, 22 Jan 2020 03:48:47 GMT  
		Size: 23.8 MB (23817324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc9352f6727d37e9b3c1c27b16c1ed2d719e1063008fc014e0583c3c3b4e062`  
		Last Modified: Wed, 22 Jan 2020 03:48:41 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; 386

```console
$ docker pull nginx@sha256:45f818575b4766e6b72da33b57e84e5a6885c658fc1e66c0e8f7d2b4049cdeea
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52265013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa531e52374f58852347bbfc1b08dfe97c82cf62e7a9cc06cec60c2d7404aa59`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:35 GMT
ADD file:447f0758c9f5653f03d964e54a38c18f24cf4c43e05fc38e7a76aebd6d6bafa8 in / 
# Sat, 28 Dec 2019 04:39:35 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 09:07:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Sat, 28 Dec 2019 09:08:43 GMT
ENV NGINX_VERSION=1.16.1
# Wed, 22 Jan 2020 05:02:03 GMT
ENV NJS_VERSION=0.3.8
# Wed, 22 Jan 2020 05:02:04 GMT
ENV PKG_RELEASE=1~buster
# Wed, 22 Jan 2020 05:02:27 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base     && apt-get remove --purge --auto-remove -y ca-certificates && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi
# Wed, 22 Jan 2020 05:02:28 GMT
RUN ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log
# Wed, 22 Jan 2020 05:02:28 GMT
EXPOSE 80
# Wed, 22 Jan 2020 05:02:29 GMT
STOPSIGNAL SIGTERM
# Wed, 22 Jan 2020 05:02:29 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5536417213b9f46f2118943c1151912954d6077afe03a32e68521774cc358095`  
		Last Modified: Sat, 28 Dec 2019 04:44:24 GMT  
		Size: 27.7 MB (27747020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb21dfa250a2412366f24c4ebc5dc1354ccae1151bb4b1921c31663d3b27951`  
		Last Modified: Wed, 22 Jan 2020 05:11:26 GMT  
		Size: 24.5 MB (24517790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e7e1a3abd296db8e01e37c529dec9e685ade8d7c6604b5bb5afaec51976af8`  
		Last Modified: Wed, 22 Jan 2020 05:11:20 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; ppc64le

```console
$ docker pull nginx@sha256:57697e43a14e0ae530d7c0f72405796b70d0e4388390c2c92af2c9d668ebfd39
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56030943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbb4a46402bed42fa8f0b86bc9058965275097afbc20a90e2239e6a25257439`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:abec4f3d6a54bb0725560d826d07e99da3d6b582433c6dd95605626c67d7c2d6 in / 
# Sat, 28 Dec 2019 04:20:43 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:47:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Sat, 28 Dec 2019 09:04:05 GMT
ENV NGINX_VERSION=1.16.1
# Wed, 22 Jan 2020 03:16:31 GMT
ENV NJS_VERSION=0.3.8
# Wed, 22 Jan 2020 03:16:33 GMT
ENV PKG_RELEASE=1~buster
# Wed, 22 Jan 2020 03:24:53 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base     && apt-get remove --purge --auto-remove -y ca-certificates && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi
# Wed, 22 Jan 2020 03:25:00 GMT
RUN ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log
# Wed, 22 Jan 2020 03:25:02 GMT
EXPOSE 80
# Wed, 22 Jan 2020 03:25:04 GMT
STOPSIGNAL SIGTERM
# Wed, 22 Jan 2020 03:25:06 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:37e6f4d596ea5c3cc92914bd95508a4192c8834c4edaff414734885929b07800`  
		Last Modified: Sat, 28 Dec 2019 04:28:05 GMT  
		Size: 30.5 MB (30517529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6793f6aeb00a752b2b8ea5fef5ec730595fba398facff26538ba255b7d2ad215`  
		Last Modified: Wed, 22 Jan 2020 03:42:11 GMT  
		Size: 25.5 MB (25513210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d77cf5f985b3896c69375f4f83790fa9c0d365df90d79d2ebf18022e0d89797`  
		Last Modified: Wed, 22 Jan 2020 03:42:05 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; s390x

```console
$ docker pull nginx@sha256:d89fc34153a0a217611c04afc5e2878790f2030e4de09b24eb5e3ac822d3c764
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49200854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aebeb5d0f1e3a785257d03672068a941aea289fe16bdedee73bde737c55a6b1`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:03 GMT
ADD file:eec6c56f8680753860198c3af0d94aabb87018ca30f6f6e346621a6bffe0e4b8 in / 
# Sat, 28 Dec 2019 04:42:04 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:53:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Sat, 28 Dec 2019 06:58:45 GMT
ENV NGINX_VERSION=1.16.1
# Wed, 22 Jan 2020 02:41:22 GMT
ENV NJS_VERSION=0.3.8
# Wed, 22 Jan 2020 02:41:23 GMT
ENV PKG_RELEASE=1~buster
# Wed, 22 Jan 2020 02:43:52 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base     && apt-get remove --purge --auto-remove -y ca-certificates && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi
# Wed, 22 Jan 2020 02:43:53 GMT
RUN ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log
# Wed, 22 Jan 2020 02:43:53 GMT
EXPOSE 80
# Wed, 22 Jan 2020 02:43:53 GMT
STOPSIGNAL SIGTERM
# Wed, 22 Jan 2020 02:43:53 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f7542f43e95fb32a870ee38d7f0e7bb23267ac8dcf709e3944311b0a30d7a479`  
		Last Modified: Sat, 28 Dec 2019 04:45:08 GMT  
		Size: 25.7 MB (25705315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82492f8551e61439248d69d12118d50ee22aea2cc5bcc0912318aca1c56684c0`  
		Last Modified: Wed, 22 Jan 2020 02:52:26 GMT  
		Size: 23.5 MB (23495334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fdd206738c20a24b20c544e043e0b13e4b3ff7583ee6f2e067271ad1e0ca9a`  
		Last Modified: Wed, 22 Jan 2020 02:52:23 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

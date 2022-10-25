## `nginx:stable`

```console
$ docker pull nginx@sha256:101c50ae30f29b1fbe3410339a3a5e173e7fb57e9ca8f5d1877c511a706a1270
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
$ docker pull nginx@sha256:916bf7632e359af7d6b3b589068cde5df6ac801d30bbade67f79468f2e54bd0b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56818857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3894511a33dc539e2adcf2aa94a422e3962e2c8f27eaf9b90307e1ff54158567`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:44:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 19 Oct 2022 18:21:11 GMT
ENV NGINX_VERSION=1.22.1
# Wed, 19 Oct 2022 18:21:11 GMT
ENV NJS_VERSION=0.7.7
# Wed, 19 Oct 2022 18:21:11 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 19 Oct 2022 18:21:29 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 19 Oct 2022 18:21:29 GMT
COPY file:7b307b62e82255f040c9812421a30090bf9abf3685f27b02d77fcca99f997911 in / 
# Wed, 19 Oct 2022 18:21:29 GMT
COPY file:5c18272734349488bd0c94ec8d382c872c1a0a435cca13bd4671353d6021d2cb in /docker-entrypoint.d 
# Wed, 19 Oct 2022 18:21:30 GMT
COPY file:abbcbf84dc17ee4454b6b2e3cf914be88e02cf84d344ec45a5b31235379d722a in /docker-entrypoint.d 
# Wed, 19 Oct 2022 18:21:30 GMT
COPY file:e57eef017a414ca793499729d80a7b9075790c9a804f930f1417e56d506970cf in /docker-entrypoint.d 
# Wed, 19 Oct 2022 18:21:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Oct 2022 18:21:30 GMT
EXPOSE 80
# Wed, 19 Oct 2022 18:21:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Oct 2022 18:21:30 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6696a2de2c32ee8ed6d0590c774e15e55c4e5bef40bc58754cbe431116c6a5`  
		Last Modified: Wed, 19 Oct 2022 18:24:21 GMT  
		Size: 25.4 MB (25394996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48f8d36bdd30c10e2e564b89515be167025772d203a12c37c1b1ba3a0ca0475`  
		Last Modified: Wed, 19 Oct 2022 18:24:18 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f41668780596abc05b8f8ecddec13e3db4b02da9bd27312c400ad640456fac`  
		Last Modified: Wed, 19 Oct 2022 18:24:18 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4320b2c3fadebc73b06688def290ee069175cf83880b6adda9fb4a368165ec2`  
		Last Modified: Wed, 19 Oct 2022 18:24:18 GMT  
		Size: 772.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b10870232f6b7aea2ef3262fcd1574121cd3ddfbed02e9c0f2a49e08f81337`  
		Last Modified: Wed, 19 Oct 2022 18:24:18 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; arm variant v5

```console
$ docker pull nginx@sha256:c08bcb8e880cbc082affdbe582f71a0cbd87691bacbd1ffd59a6007248c17755
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53493954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2693718f7e888852a221f1d596e18b5463d0d55e4215b5106c7c6c0e1099494`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 25 Oct 2022 03:06:35 GMT
ADD file:015ddb23f9ceec681c3a46b6d48671071fd41c5d56a957f6c96b50b1fc089a36 in / 
# Tue, 25 Oct 2022 03:06:38 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:34:48 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 25 Oct 2022 06:43:14 GMT
ENV NGINX_VERSION=1.22.1
# Tue, 25 Oct 2022 06:43:14 GMT
ENV NJS_VERSION=0.7.7
# Tue, 25 Oct 2022 06:43:14 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 25 Oct 2022 06:46:55 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 25 Oct 2022 06:46:55 GMT
COPY file:7b307b62e82255f040c9812421a30090bf9abf3685f27b02d77fcca99f997911 in / 
# Tue, 25 Oct 2022 06:46:55 GMT
COPY file:5c18272734349488bd0c94ec8d382c872c1a0a435cca13bd4671353d6021d2cb in /docker-entrypoint.d 
# Tue, 25 Oct 2022 06:46:55 GMT
COPY file:abbcbf84dc17ee4454b6b2e3cf914be88e02cf84d344ec45a5b31235379d722a in /docker-entrypoint.d 
# Tue, 25 Oct 2022 06:46:55 GMT
COPY file:e57eef017a414ca793499729d80a7b9075790c9a804f930f1417e56d506970cf in /docker-entrypoint.d 
# Tue, 25 Oct 2022 06:46:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 06:46:56 GMT
EXPOSE 80
# Tue, 25 Oct 2022 06:46:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Oct 2022 06:46:56 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:0df644382ba7fd23e9e4166ec2a03ec88b6cc5f640fb45413ecd913ceb901e41`  
		Last Modified: Tue, 25 Oct 2022 03:11:52 GMT  
		Size: 28.9 MB (28918513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41c24bcfe6619e663bc68c4e3f0e88f98bf62c2ad28b63c174c7098099ad4ca`  
		Last Modified: Tue, 25 Oct 2022 06:53:09 GMT  
		Size: 24.6 MB (24571678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a80bb748f8b46e373595cb21f2d2d33c9ef9c5ae2ae1f763946d6302730262d`  
		Last Modified: Tue, 25 Oct 2022 06:53:05 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d92b0a04ced36a016df4b7f6516463510ac9194ab789d0480fc0fc84f447ad`  
		Last Modified: Tue, 25 Oct 2022 06:53:05 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471976bb1ebd0e3cf8e71c47c3707071c1e746a604f2e54a362ce5b17108f9c1`  
		Last Modified: Tue, 25 Oct 2022 06:53:05 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94724b4714cef5c3828ef169ebd617779733369699f3652eefc789d9e630d4a`  
		Last Modified: Tue, 25 Oct 2022 06:53:05 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; arm variant v7

```console
$ docker pull nginx@sha256:e345533d788cd876ac8abe98e458f921beab72dcde9e966f9e8d70dc3925f1da
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50296284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497149fbfcaf0994bf60685642c0c354190c68b9b483c86a4db894fe48aa6fcd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 08:14:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 19 Oct 2022 18:23:28 GMT
ENV NGINX_VERSION=1.22.1
# Wed, 19 Oct 2022 18:23:28 GMT
ENV NJS_VERSION=0.7.7
# Wed, 19 Oct 2022 18:23:28 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 19 Oct 2022 18:27:36 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 19 Oct 2022 18:27:36 GMT
COPY file:7b307b62e82255f040c9812421a30090bf9abf3685f27b02d77fcca99f997911 in / 
# Wed, 19 Oct 2022 18:27:36 GMT
COPY file:5c18272734349488bd0c94ec8d382c872c1a0a435cca13bd4671353d6021d2cb in /docker-entrypoint.d 
# Wed, 19 Oct 2022 18:27:36 GMT
COPY file:abbcbf84dc17ee4454b6b2e3cf914be88e02cf84d344ec45a5b31235379d722a in /docker-entrypoint.d 
# Wed, 19 Oct 2022 18:27:37 GMT
COPY file:e57eef017a414ca793499729d80a7b9075790c9a804f930f1417e56d506970cf in /docker-entrypoint.d 
# Wed, 19 Oct 2022 18:27:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Oct 2022 18:27:37 GMT
EXPOSE 80
# Wed, 19 Oct 2022 18:27:37 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Oct 2022 18:27:37 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e005479f2e53c7730035f6b421b432190690af0d17fd3cbcb1811d44e87610`  
		Last Modified: Wed, 19 Oct 2022 18:43:01 GMT  
		Size: 23.7 MB (23713324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b3042e809c195cc6fc0792d4f96d1c9291b2588e59b507c2f684d2143e2684`  
		Last Modified: Wed, 19 Oct 2022 18:42:57 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3be60561f4f88c80d3a769a12bf2ffb8edb65cbe038fb774f5a3aed95098e8`  
		Last Modified: Wed, 19 Oct 2022 18:42:57 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86569439811721ba5200bbf0ef77f5c31d01763d10b54ea04346e5d002ab14c5`  
		Last Modified: Wed, 19 Oct 2022 18:42:57 GMT  
		Size: 773.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05a2ea5b1b6f344809452ecc260f646778410946a97fc79ee859e6008c2e1ef`  
		Last Modified: Wed, 19 Oct 2022 18:42:57 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:475c74ea59af5df4d2f38152df31b864bb237f0a5e915fbd94b5340736d36329
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.4 MB (55388121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2e5668de0c855bea62b6bf34de3b1f168d7435f78e80f9d87b33ef011f919f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:25:39 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 19 Oct 2022 17:42:14 GMT
ENV NGINX_VERSION=1.22.1
# Wed, 19 Oct 2022 17:42:15 GMT
ENV NJS_VERSION=0.7.7
# Wed, 19 Oct 2022 17:42:16 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 19 Oct 2022 17:42:34 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 19 Oct 2022 17:42:35 GMT
COPY file:7b307b62e82255f040c9812421a30090bf9abf3685f27b02d77fcca99f997911 in / 
# Wed, 19 Oct 2022 17:42:36 GMT
COPY file:5c18272734349488bd0c94ec8d382c872c1a0a435cca13bd4671353d6021d2cb in /docker-entrypoint.d 
# Wed, 19 Oct 2022 17:42:37 GMT
COPY file:abbcbf84dc17ee4454b6b2e3cf914be88e02cf84d344ec45a5b31235379d722a in /docker-entrypoint.d 
# Wed, 19 Oct 2022 17:42:38 GMT
COPY file:e57eef017a414ca793499729d80a7b9075790c9a804f930f1417e56d506970cf in /docker-entrypoint.d 
# Wed, 19 Oct 2022 17:42:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Oct 2022 17:42:39 GMT
EXPOSE 80
# Wed, 19 Oct 2022 17:42:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Oct 2022 17:42:41 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efeccca276f245a2a28f3f81aa088b274e4156f3e08ea3b4608ae74ad31c82`  
		Last Modified: Wed, 19 Oct 2022 17:46:46 GMT  
		Size: 25.3 MB (25319964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f01e3fde422714c96c60e40252e84912b2a7984a7dd58a63b61788a4d8f10ab`  
		Last Modified: Wed, 19 Oct 2022 17:46:43 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf673636f44fbbff92753ead91b3d738e9ece42a701dd72483e11884c6116b80`  
		Last Modified: Wed, 19 Oct 2022 17:46:43 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d81d47e60cc9b31e94ca80437b258da8151b532cf498e722a93873e84f78ff`  
		Last Modified: Wed, 19 Oct 2022 17:46:43 GMT  
		Size: 773.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9226adc69b6bf0ba59abc8fa18f0176f037f56ee78b71f4342e9947543110d8`  
		Last Modified: Wed, 19 Oct 2022 17:46:43 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; 386

```console
$ docker pull nginx@sha256:acd8354bf6d97290d7337d1da0c4a6b3985f13c9787530180c36d9f7d4fe5927
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58709621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2610e1cbc9ba80314b09d6ccd7f88def9ab39a9b79276b8e10a8f37822f9bca5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:18:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 19 Oct 2022 17:53:00 GMT
ENV NGINX_VERSION=1.22.1
# Wed, 19 Oct 2022 17:53:01 GMT
ENV NJS_VERSION=0.7.7
# Wed, 19 Oct 2022 17:53:02 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 19 Oct 2022 17:56:06 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 19 Oct 2022 17:56:07 GMT
COPY file:7b307b62e82255f040c9812421a30090bf9abf3685f27b02d77fcca99f997911 in / 
# Wed, 19 Oct 2022 17:56:08 GMT
COPY file:5c18272734349488bd0c94ec8d382c872c1a0a435cca13bd4671353d6021d2cb in /docker-entrypoint.d 
# Wed, 19 Oct 2022 17:56:09 GMT
COPY file:abbcbf84dc17ee4454b6b2e3cf914be88e02cf84d344ec45a5b31235379d722a in /docker-entrypoint.d 
# Wed, 19 Oct 2022 17:56:10 GMT
COPY file:e57eef017a414ca793499729d80a7b9075790c9a804f930f1417e56d506970cf in /docker-entrypoint.d 
# Wed, 19 Oct 2022 17:56:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Oct 2022 17:56:11 GMT
EXPOSE 80
# Wed, 19 Oct 2022 17:56:12 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Oct 2022 17:56:13 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0028ce36705dca9a0ff79743480fd1f5a09bfcef455e9c3e1544300f68fc2a`  
		Last Modified: Wed, 19 Oct 2022 18:09:39 GMT  
		Size: 26.3 MB (26309569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81e79c9d22917bfa5596cee731808be62f22805a9ad41db34ee8aa885917076`  
		Last Modified: Wed, 19 Oct 2022 18:09:36 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28b04c1ffdb296ac4744ca84c3c5fe00f1a89200c7cab3425e1c5bbb6fe8d0e`  
		Last Modified: Wed, 19 Oct 2022 18:09:36 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc8f9437406a0c424c60137cfb331f6db285e463c912fe61fb191161bfcd8c7`  
		Last Modified: Wed, 19 Oct 2022 18:09:36 GMT  
		Size: 773.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de1a8d24d8ceb723ff3853393683f2df615eac64cf467a21d75022753febf8f`  
		Last Modified: Wed, 19 Oct 2022 18:09:36 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; mips64le

```console
$ docker pull nginx@sha256:3365b007374afa9333f43a66fecb78bad1b60e904d68f0703fe9d6741a1d5694
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54931883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338f729ee18eb0320479b2467cba865d29823eeeada908f8aab2fc1ab976f5e1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Oct 2022 00:10:26 GMT
ADD file:48da6b2f4e0315e4f502001a00e4b2abb58d553de11a41901ba859a461052bea in / 
# Wed, 05 Oct 2022 00:10:29 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 07:55:41 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 19 Oct 2022 18:39:30 GMT
ENV NGINX_VERSION=1.22.1
# Wed, 19 Oct 2022 18:39:32 GMT
ENV NJS_VERSION=0.7.7
# Wed, 19 Oct 2022 18:39:34 GMT
ENV PKG_RELEASE=1~bullseye
# Wed, 19 Oct 2022 18:54:26 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 19 Oct 2022 18:54:28 GMT
COPY file:7b307b62e82255f040c9812421a30090bf9abf3685f27b02d77fcca99f997911 in / 
# Wed, 19 Oct 2022 18:54:30 GMT
COPY file:5c18272734349488bd0c94ec8d382c872c1a0a435cca13bd4671353d6021d2cb in /docker-entrypoint.d 
# Wed, 19 Oct 2022 18:54:32 GMT
COPY file:abbcbf84dc17ee4454b6b2e3cf914be88e02cf84d344ec45a5b31235379d722a in /docker-entrypoint.d 
# Wed, 19 Oct 2022 18:54:34 GMT
COPY file:e57eef017a414ca793499729d80a7b9075790c9a804f930f1417e56d506970cf in /docker-entrypoint.d 
# Wed, 19 Oct 2022 18:54:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Oct 2022 18:54:39 GMT
EXPOSE 80
# Wed, 19 Oct 2022 18:54:41 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Oct 2022 18:54:44 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3288c6e2e7130a1e313203f049bde0e57a05237441a3cab92c27f9ada139315b`  
		Last Modified: Wed, 05 Oct 2022 00:18:36 GMT  
		Size: 29.6 MB (29640851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c36a860d3e91413c6e82c8e9e69d72e3bce2a9b45f67bac05b8ba39c62076`  
		Last Modified: Wed, 19 Oct 2022 19:14:15 GMT  
		Size: 25.3 MB (25287270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec60b80ef64d0a5392a7c3598ca791dea949d6533df814e342728c2485bc850`  
		Last Modified: Wed, 19 Oct 2022 19:13:56 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e29f3885e9251dda61c1acc06ad9d633cbc6e045670933cb8cac824b3b74d3`  
		Last Modified: Wed, 19 Oct 2022 19:13:58 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d417d8a05ddbf556b9aac06b12ceb3b2208e0c6e82b372934ba49206c1cc3f`  
		Last Modified: Wed, 19 Oct 2022 19:13:57 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810736908b322a90c06b018d049a4e20d146316ceac89d7472d89de05f2b19ac`  
		Last Modified: Wed, 19 Oct 2022 19:13:57 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; ppc64le

```console
$ docker pull nginx@sha256:34ec6f5e8a536c0052fc3a32a770ac9e06998398774476fc703768bbcda89121
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62597881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0096fe970298ddee99542b0a045464022747684b76dad77ae199a109e8d68c17`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:30 GMT
ADD file:3a95a896d463569ce82199957052b3467123a4bd3385a0a4e397cf08402a99c3 in / 
# Tue, 02 Aug 2022 01:17:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:54:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 02 Aug 2022 04:02:09 GMT
ENV NGINX_VERSION=1.22.0
# Tue, 02 Aug 2022 04:02:10 GMT
ENV NJS_VERSION=0.7.6
# Tue, 02 Aug 2022 04:02:10 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 09 Aug 2022 19:14:56 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Aug 2022 19:14:58 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 09 Aug 2022 19:14:58 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 09 Aug 2022 19:14:59 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Aug 2022 19:14:59 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 09 Aug 2022 19:14:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 19:14:59 GMT
EXPOSE 80
# Tue, 09 Aug 2022 19:15:00 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 19:15:00 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5241cd116d6e6e2d62f3d8c2245b74daca9f6cc154eaccd738feb41984c74714`  
		Last Modified: Tue, 02 Aug 2022 01:24:39 GMT  
		Size: 35.3 MB (35272771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647106ac8587beea139fa517acd17ce60a6a516cd49e46614cab9c5847bd2ddb`  
		Last Modified: Tue, 09 Aug 2022 19:33:38 GMT  
		Size: 27.3 MB (27321549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8dc722f70c9ad1594f76e45bfe941b11aca2565252f6f35bba51c464ac44f7`  
		Last Modified: Tue, 09 Aug 2022 19:33:31 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7974ad9701a87df694f7863b1efb8e9ade825d2ed9ec65647aa36870426b4bd8`  
		Last Modified: Tue, 09 Aug 2022 19:33:31 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8cbbfcc5e4cd196839f8b6838b643bbd4502c24b2c2cc3c64a9fc705db01c7`  
		Last Modified: Tue, 09 Aug 2022 19:33:31 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62506525c1e42cd2feb726b7381645cad344127ee668bb09f4932bb8b8ef3cd1`  
		Last Modified: Tue, 09 Aug 2022 19:33:31 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; s390x

```console
$ docker pull nginx@sha256:0becac1b6bbbd63c193e70ba7f1c25eb1a2a93962311f28a4b33da618779a569
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54822900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a363e6be98cb73b239348a9a9614f96cc1a1a49b558d426b8c086c9c003d58e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 04 Oct 2022 23:42:42 GMT
ADD file:7acfe92be51da9cffeb5b063cc87926d1ce457729e3080de340603a38216a708 in / 
# Tue, 04 Oct 2022 23:42:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:27:04 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 05 Oct 2022 01:31:12 GMT
ENV NGINX_VERSION=1.22.0
# Wed, 05 Oct 2022 01:31:13 GMT
ENV NJS_VERSION=0.7.6
# Wed, 05 Oct 2022 01:31:13 GMT
ENV PKG_RELEASE=1~bullseye
# Thu, 06 Oct 2022 21:08:14 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Thu, 06 Oct 2022 21:08:15 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Thu, 06 Oct 2022 21:08:16 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Thu, 06 Oct 2022 21:08:16 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Thu, 06 Oct 2022 21:08:16 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Thu, 06 Oct 2022 21:08:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Oct 2022 21:08:16 GMT
EXPOSE 80
# Thu, 06 Oct 2022 21:08:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 21:08:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:62990b94a520bfcf718ec711f8444f83c536af2c83c8e53fdfe1f89fdcb79826`  
		Last Modified: Tue, 04 Oct 2022 23:47:16 GMT  
		Size: 29.7 MB (29650719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf512749e8dc3eb0149d365bbfb40439e286eb5bbbedfde5851dc49840dc3aa`  
		Last Modified: Thu, 06 Oct 2022 21:18:52 GMT  
		Size: 25.2 MB (25168623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b9acab39466753ac951d8823f1724b9c2fbd0279e9e3fee726245f81c6d56a`  
		Last Modified: Thu, 06 Oct 2022 21:18:52 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a861f14704cccb1e4423448355a3e6a1fd441a11613b09b9900b73f9a5e2a7`  
		Last Modified: Thu, 06 Oct 2022 21:18:52 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f345976bc12988901b85f4b3b3570821f4f4a6ca8a31993604c95ce79526f124`  
		Last Modified: Thu, 06 Oct 2022 21:18:52 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1beffabe206cb709099d9680a2ea763c7052457dcc7fd3c14fb2455697f61bd`  
		Last Modified: Thu, 06 Oct 2022 21:18:48 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

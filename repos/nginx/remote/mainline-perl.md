## `nginx:mainline-perl`

```console
$ docker pull nginx@sha256:1119f6367b529ad5fbfc0f1fd0c4e560914cdc187f400a0cde77824c621aaf14
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

### `nginx:mainline-perl` - linux; amd64

```console
$ docker pull nginx@sha256:83247be27bd1fc295b196f56c7909d0a2133f180ea947fa12151dace77b00627
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64635993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e41be1367f5619952b9e395aec4054cca3b0fbe203e7cb9982200422bfc55de`
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
# Fri, 12 Mar 2021 12:34:39 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 12 Mar 2021 12:34:40 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 12 Mar 2021 12:34:40 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 12 Mar 2021 12:34:40 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 12 Mar 2021 12:34:40 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 12 Mar 2021 12:34:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Mar 2021 12:34:41 GMT
EXPOSE 80
# Fri, 12 Mar 2021 12:34:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Mar 2021 12:34:41 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21444789c32ca41aac17983fc2ae5b29fa33157de2faafb65ba147b61ecbd928`  
		Last Modified: Fri, 12 Mar 2021 12:37:10 GMT  
		Size: 37.5 MB (37531419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c81cbfa727a5d0ca5723b4480e025e689aed2e3697f3f7ee74fe4ef266d5e54`  
		Last Modified: Fri, 12 Mar 2021 12:37:00 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db939fa2a78a4e39000b53ae097c12fa7547530658f94a22a28600579d21cf68`  
		Last Modified: Fri, 12 Mar 2021 12:37:00 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3461f2b446fc22d2fd073d874814021e7036b3f7e0146bcdd7cd8b64bceee57d`  
		Last Modified: Fri, 12 Mar 2021 12:37:00 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420dcfb4af9d4283aa6e40e17c7154a8f3f95f4119d1d7ac802a883258e9758e`  
		Last Modified: Fri, 12 Mar 2021 12:37:00 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:dc745b385e520063de67edbe7a678e67f45951a6a39a622c2bf48b9248ac8026
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60568709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada20cc0de40befd72c7845a4e4e7ad6ea0c49a89519ec7c034313e1ce3ecbef`
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
# Fri, 26 Mar 2021 10:01:11 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 26 Mar 2021 10:01:13 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 26 Mar 2021 10:01:15 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 26 Mar 2021 10:01:17 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 26 Mar 2021 10:01:18 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 26 Mar 2021 10:01:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 10:01:21 GMT
EXPOSE 80
# Fri, 26 Mar 2021 10:01:23 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 10:01:24 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:997e59852ec0e1a23e4a179db14793947d60390c392ce15abc0f811e797c49ca`  
		Last Modified: Fri, 26 Mar 2021 08:00:22 GMT  
		Size: 24.8 MB (24846159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b025c05f84f355388fa64228fd75c9c6f714d09650c6f5d9c78af1726693bc`  
		Last Modified: Fri, 26 Mar 2021 10:17:59 GMT  
		Size: 35.7 MB (35718972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777b696abe98e956dcac5736cf5af2d684d867e2dd55e63996eb8f2cd6c8a2aa`  
		Last Modified: Fri, 26 Mar 2021 10:17:45 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f981df9eb66cbe8233549265810e27d04b85ba6a17594f6dfadf4449c5c9c51`  
		Last Modified: Fri, 26 Mar 2021 10:17:44 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08a75fd2a9eaed4323749f28326733fe5618c4eca8e4414710d4efed00d9413`  
		Last Modified: Fri, 26 Mar 2021 10:17:44 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a9202f56eed85c31a6743edee0bb4ca765ba9f9e7597d328c5e0f2e0387046`  
		Last Modified: Fri, 26 Mar 2021 10:17:44 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:ef2ee20b413fabacd92054ac06fa72dad0b291f9b3204c0a9b64b21327d73b6e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57321546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a233939203d5043cfba6649ba3b06a4d85d396785093b96a272d98c4931b67`
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
# Fri, 12 Mar 2021 04:10:32 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 12 Mar 2021 04:10:36 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 12 Mar 2021 04:10:38 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 12 Mar 2021 04:10:40 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 12 Mar 2021 04:10:41 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 12 Mar 2021 04:10:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Mar 2021 04:10:42 GMT
EXPOSE 80
# Fri, 12 Mar 2021 04:10:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Mar 2021 04:10:43 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:e12d26f75fe8b7fd14712965ff5178762227d07d2151bb35fa21105ddfc4a14a`  
		Last Modified: Fri, 12 Mar 2021 02:10:28 GMT  
		Size: 22.7 MB (22709467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1515b260b35bf09db40630c53ca2ccf77380c4e9461b2cc9f526b4b7b998f94a`  
		Last Modified: Fri, 12 Mar 2021 04:25:12 GMT  
		Size: 34.6 MB (34608505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1086b01845bed1cdc8f6916e1914d9d586571453549429eaf072544df7d63`  
		Last Modified: Fri, 12 Mar 2021 04:25:00 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eef08da7a8602c324d4782d4e0a277aacbb6aa7b79d34c30e0d05b0cd17fb93`  
		Last Modified: Fri, 12 Mar 2021 04:25:00 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a054d939aebc1bad1253554a915f7fec2a114d2ea52799082412dc6a9bbf93`  
		Last Modified: Fri, 12 Mar 2021 04:25:00 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31a16a48b630a5f5cbc0e1001801bdccd7d0218f8623108611a218d59c9834b`  
		Last Modified: Fri, 12 Mar 2021 04:25:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:85f81515850d7f788937aa55bcda8d046a606dea3756511dbdefb5c04bfcba92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63094978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e126860b498124bdbd469813dde25fc57379a62961d587022a25b751592495`
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
# Fri, 12 Mar 2021 06:02:08 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 12 Mar 2021 06:02:10 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 12 Mar 2021 06:02:11 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 12 Mar 2021 06:02:13 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 12 Mar 2021 06:02:14 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 12 Mar 2021 06:02:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Mar 2021 06:02:18 GMT
EXPOSE 80
# Fri, 12 Mar 2021 06:02:19 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Mar 2021 06:02:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:706ee5d0a6b53d9257cbea22d8409fb22c867ab3a001c65f6b8bfd37dace0e58`  
		Last Modified: Fri, 12 Mar 2021 02:01:39 GMT  
		Size: 25.9 MB (25856512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09af2bcc1c2412b976e6f97eda52829759cdabfd4df1e99e5bc7939e58155f30`  
		Last Modified: Fri, 12 Mar 2021 06:06:04 GMT  
		Size: 37.2 MB (37234893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fcc002e5a2081b5097fa46fa4cf9557753bd912cb234a22f333fb421f077a`  
		Last Modified: Fri, 12 Mar 2021 06:05:53 GMT  
		Size: 599.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169e389ad42c94b5a9e6e4cb805bd18dd20856502532f2d179308badcb6e96d2`  
		Last Modified: Fri, 12 Mar 2021 06:05:54 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06f9bbffc2ef7cde92f42c5884a622ab8d7706453c272704b204019adbcf885`  
		Last Modified: Fri, 12 Mar 2021 06:05:54 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05944cb7264abbbd695f364ff45aade460376a3ab88a592896fd4ff6ca8a61f4`  
		Last Modified: Fri, 12 Mar 2021 06:05:53 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-perl` - linux; 386

```console
$ docker pull nginx@sha256:aeaab81e6c5b3a7fdc38c2df4a38d94666022a598a9f0163c204a9594dba49bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65625266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de940d7c8b5a4db93a27cd07a0fa79ad867337329058243c12591344d2cc1c5`
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
# Fri, 12 Mar 2021 13:42:29 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 12 Mar 2021 13:42:30 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 12 Mar 2021 13:42:30 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 12 Mar 2021 13:42:30 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 12 Mar 2021 13:42:30 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 12 Mar 2021 13:42:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Mar 2021 13:42:31 GMT
EXPOSE 80
# Fri, 12 Mar 2021 13:42:31 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Mar 2021 13:42:31 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:0898aa7472f57f223652846337cf862f142e109d0c039b41886e7f20c345f85e`  
		Last Modified: Fri, 12 Mar 2021 01:52:08 GMT  
		Size: 27.8 MB (27760948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e838d57f39ea15e7875179b7fe6bfb891e0e21bc2e5b7e6d2d938e5438e7c6`  
		Last Modified: Fri, 12 Mar 2021 13:45:50 GMT  
		Size: 37.9 MB (37860745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82502a33da64e36d60209c8e9b8d482058b5cae5b97356c488749f53722a7b55`  
		Last Modified: Fri, 12 Mar 2021 13:45:43 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0e9611d5b0a9cf52e7a9555159a092b3315a3d57a07a9adf4e2ba36cf5521b`  
		Last Modified: Fri, 12 Mar 2021 13:45:42 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37e32d448864e828e90e3944a29142cb8aac481090ee29a161a314585860812`  
		Last Modified: Fri, 12 Mar 2021 13:45:43 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da43dfbe795aa19f549f8b0b465dedb8eb5e612c5abf6ea6ec64eeb274dece7`  
		Last Modified: Fri, 12 Mar 2021 13:45:45 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-perl` - linux; mips64le

```console
$ docker pull nginx@sha256:066c56fe75d967dbfd41264feb99d30699ffe659734e2bbfc4111d1dab375710
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62126830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cffc60f7740a7cdd60f4211394c3423c878f0a3bb0b53f6512ca71dc397242`
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
# Fri, 26 Mar 2021 11:34:05 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 26 Mar 2021 11:34:06 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 26 Mar 2021 11:34:06 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 26 Mar 2021 11:34:07 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 26 Mar 2021 11:34:07 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 26 Mar 2021 11:34:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 11:34:08 GMT
EXPOSE 80
# Fri, 26 Mar 2021 11:34:08 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 11:34:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5f863e006c40853ec8c23aa5b7a0e95918001f96878fb45770410ac4df51cf88`  
		Last Modified: Fri, 26 Mar 2021 08:16:29 GMT  
		Size: 25.8 MB (25772487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9dffa3c02884a0101e9780740d48bf67f50d1d8cb71ba4e7534af6cbeda64c`  
		Last Modified: Fri, 26 Mar 2021 11:59:07 GMT  
		Size: 36.4 MB (36350771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d127a93898b883721b4820f5decb01687143db4927b612c38ca8fff5715109e4`  
		Last Modified: Fri, 26 Mar 2021 11:58:41 GMT  
		Size: 599.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d228ba2bb6d0ceccb9fd9417dd21561d622decc3bf05fa9651ae274316deec40`  
		Last Modified: Fri, 26 Mar 2021 11:58:41 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b219371dc944704e39b800267f91b55c1f1d087ea17ff5f177669647a4facbee`  
		Last Modified: Fri, 26 Mar 2021 11:58:42 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4568cacce9b9c429947c9a216fd6c5ae460833052cd3de873dc235cb59f5b9c9`  
		Last Modified: Fri, 26 Mar 2021 11:58:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:f8d4738c1cbcbc40340a2e7af5512590642b1dd41689b67aad8838027f3bdebd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70349703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed46a42f08a6b90257cd6a59473cfcb2ae7bed9a70490537ed6a493870cb730a`
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
# Fri, 12 Mar 2021 07:25:52 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 12 Mar 2021 07:26:00 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 12 Mar 2021 07:26:03 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 12 Mar 2021 07:26:05 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 12 Mar 2021 07:26:06 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 12 Mar 2021 07:26:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Mar 2021 07:26:14 GMT
EXPOSE 80
# Fri, 12 Mar 2021 07:26:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Mar 2021 07:26:27 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:1d686056fdac1848f4fd78ba2b335502055ffe98c79619e21d0c2fb7db95257e`  
		Last Modified: Fri, 12 Mar 2021 02:45:35 GMT  
		Size: 30.5 MB (30525728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9892dd6ae5a364a15cba246fe4fba9ab29efa3ca0ed71f433bf30c357f7c71bb`  
		Last Modified: Fri, 12 Mar 2021 08:20:40 GMT  
		Size: 39.8 MB (39820398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8316e7d5d884a367b9161dd28057c25614a7bf89349277968176fb4c4e98e378`  
		Last Modified: Fri, 12 Mar 2021 08:20:31 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f185ac00a0efe830f9b9b8f7fb24e073a33086993fc10d4699002437086ce5`  
		Last Modified: Fri, 12 Mar 2021 08:20:32 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b446210e0f8021718be23b968c973a394b8a901977bfe8fd3726d924d52106f`  
		Last Modified: Fri, 12 Mar 2021 08:20:32 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b867371facd66b408e720b84e2784df55b568cd6ac74c05d8c45cf38cdc84d00`  
		Last Modified: Fri, 12 Mar 2021 08:20:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-perl` - linux; s390x

```console
$ docker pull nginx@sha256:26d8ae007d71a56de863595115b977b6a91aea4db7b3dafe14901f9723312d15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63124716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41955e822500c8a9c1796f9cfc3580b3548f84b88b2d7b579147affe0e163fa0`
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
# Fri, 26 Mar 2021 16:28:18 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 26 Mar 2021 16:28:24 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 26 Mar 2021 16:28:24 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 26 Mar 2021 16:28:25 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 26 Mar 2021 16:28:26 GMT
COPY file:c7f3907578be6851a0db02acac9e97c4d7eabda5f22a5a1ffe21139197dceb7a in /docker-entrypoint.d 
# Fri, 26 Mar 2021 16:28:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 16:28:27 GMT
EXPOSE 80
# Fri, 26 Mar 2021 16:28:27 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 16:28:27 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a37ca8d63090f0f22441ceecc0af7881a2668336202cf586e841e3d9e06f2f4b`  
		Last Modified: Fri, 26 Mar 2021 10:57:46 GMT  
		Size: 25.7 MB (25716264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2e81e15ac5e1fc7478c4f8cce4ef9cbe43b2165fbafb0ddfb91b4695b51f98`  
		Last Modified: Fri, 26 Mar 2021 16:42:41 GMT  
		Size: 37.4 MB (37404882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56e9392525f3b2d53b6f98117957f7e37410f122791157b5b72ef85bd2c1513`  
		Last Modified: Fri, 26 Mar 2021 16:42:34 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1036fb316a7758400adc04a36040a6816fa10e05d70cb40c973fe87d3ea54bca`  
		Last Modified: Fri, 26 Mar 2021 16:42:34 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134563f6b22ed730480bf5a2658cd1550fa58790ded7cacf484b424f44fc6984`  
		Last Modified: Fri, 26 Mar 2021 16:42:34 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3edf74cb497c6d4af06503dc2c7a84b9a3375c0bc634527b8ba8ee32295f42`  
		Last Modified: Fri, 26 Mar 2021 16:42:34 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

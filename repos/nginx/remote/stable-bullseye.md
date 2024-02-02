## `nginx:stable-bullseye`

```console
$ docker pull nginx@sha256:eebb35fb23a4711e3f6d7d74882edd5c35d53d510f1c01e73f24cb35cbc30a93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nginx:stable-bullseye` - linux; amd64

```console
$ docker pull nginx@sha256:b0ae11ff3fb5b59e982a4e350e587a93a22a0731f61f4ee116336a72f42327f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57026396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8963c304a2f89d2bfa055e07403bae348b293c891b8ea01f7136642eaa277a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19952d9b20829774e430d62525b9f5fc1404b8d13e888458e123b0dacf4cffb9`  
		Last Modified: Wed, 31 Jan 2024 23:54:58 GMT  
		Size: 25.6 MB (25604817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6eddd75528c512905ca8679794341fa9db1531f241a52e279f412d6e012386`  
		Last Modified: Wed, 31 Jan 2024 23:54:58 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66396a242b7e8f856be56858f5984a9d9295f059ca3a44f046c698b7b7892c7`  
		Last Modified: Wed, 31 Jan 2024 23:54:58 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be110c6aac6d6c2fd3d430acda792d5e22a160c58459891293f6250f9bcee0c0`  
		Last Modified: Wed, 31 Jan 2024 23:54:58 GMT  
		Size: 771.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871467c640a74877e224734a95efd8a600eacf6c189fe7b905f2ffa6073566da`  
		Last Modified: Wed, 31 Jan 2024 23:54:59 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:f49f4c88d6c846be9140bde0c09deb241a6a90ab771e348dcf15e8e629740b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3383bad9a7a686b22db26e3f4c5b8a1f50a404442ac758653ba1a0cf061979`

```dockerfile
```

-	Layers:
	-	`sha256:849bb355d686fc5a5630493bfbd0b2be33f089cf63a1defca0715e02acc30287`  
		Last Modified: Wed, 31 Jan 2024 23:54:58 GMT  
		Size: 2.6 MB (2587753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f42fa7b1f69792b9920952879289e5f186569ce216fb6b6c2f7896e04f3cb55`  
		Last Modified: Wed, 31 Jan 2024 23:54:58 GMT  
		Size: 27.3 KB (27325 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bullseye` - linux; arm variant v5

```console
$ docker pull nginx@sha256:40ebaea970c927b5b9da2d3cf6016d0695dc951ec05d4370e3127596a000a72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53688103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81cfe9cd646c3f4596e42de9fb830fa11c9ad50b4a527bd5921a537a6e81897`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:1b6dd4809e22729ef9f0432014187762756f1518e85ecf13db6c505bfff65308 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:dfbf1dc0873e0cde30013d8526571f69d5c53be2b8d637a6235c623cc1f66192`  
		Last Modified: Wed, 31 Jan 2024 22:48:48 GMT  
		Size: 28.9 MB (28921333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cff901a1961cc82727406933ba4283297c9e42b59678e0ad223b659cb622cd0`  
		Last Modified: Thu, 01 Feb 2024 12:12:30 GMT  
		Size: 24.8 MB (24763016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a871204449e8642e401320cea4572b945897ae7ccf6c2bcf47374a38a9a14666`  
		Last Modified: Thu, 01 Feb 2024 12:12:28 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdab4d6a0ba0bc15b938e090979d905f03840b01b6486459533949aa944b054a`  
		Last Modified: Thu, 01 Feb 2024 12:12:28 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25612a9cade4739b8f637d437424f4d6daf8a9d15a814967bc6e28fbd074f99`  
		Last Modified: Thu, 01 Feb 2024 12:12:29 GMT  
		Size: 770.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7916479edcc3704ce6abe8ed829f6c6a2389d68aa2a618f33207dc7c185e3f4`  
		Last Modified: Thu, 01 Feb 2024 12:12:30 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:7d8817008f76142507d8a55d12614c8e4b11ebf2e3223a66063faea3ebb46b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4602021e96527fe2d24423eedf8e505f443846df7c49ba070343f02d849fd6`

```dockerfile
```

-	Layers:
	-	`sha256:a4e565217de64a2d40970f40b6de935e9ef5a20aa469b99ab9a920d1279ae0af`  
		Last Modified: Thu, 01 Feb 2024 12:12:29 GMT  
		Size: 2.6 MB (2596860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5a4fc249b1537fbd268db999c47c76433e9f8320650cf6af48d6d301ab31a6`  
		Last Modified: Thu, 01 Feb 2024 12:12:28 GMT  
		Size: 27.2 KB (27245 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bullseye` - linux; arm variant v7

```console
$ docker pull nginx@sha256:c69670b77d24bf23a3888ea22419fa1653936cc6308ef881b3ffc207039d6a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50466009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b240d2b5ef20ab07e5ae411b48728afd8a4781b644a73257532e7ecced847679`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:1a36d919bfcbaa6b981b71ce99d777d303e69c2d6cb1924992e5a9cd811c11c5 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d976170654fe1bc717306b8bf14dc57d20e331b13e4797bc137e6911aa745a8a`  
		Last Modified: Thu, 11 Jan 2024 02:49:26 GMT  
		Size: 26.6 MB (26578974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac2e575f77102ea3014984c7c8123caedd067260e53ecd49601dd2c640a0459`  
		Last Modified: Fri, 12 Jan 2024 19:33:37 GMT  
		Size: 23.9 MB (23883283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f78d4ef6af89f5e0caabe73171acee963fc165fa6bf94a68f55db360fdf7de`  
		Last Modified: Fri, 12 Jan 2024 19:33:36 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b560e12c76e414f661cb882687ec655f325d2878b52d7adaffdefc70723cb72`  
		Last Modified: Fri, 12 Jan 2024 19:33:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aefd1edad5f3f2935f9f16a1b3e9f72bf37a66eed72e14af0d36e230fa9bcc`  
		Last Modified: Fri, 12 Jan 2024 19:33:37 GMT  
		Size: 770.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88335a8dedd48a0e3667d932bfe20eaac70afe0234d17e35d290af8ea8cc4c9`  
		Last Modified: Fri, 12 Jan 2024 19:33:37 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:fb32de356715030a8ceac67b8b843ca105a31a9ee358fb5f4365bbcab05dafe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f973d75ae7135f27124bcd1165e0d83fb90bd4ccb13b5fdf1598796002e3497`

```dockerfile
```

-	Layers:
	-	`sha256:78e275fa2a3ea8a93ae9f4af1644b1e2a1dc5d566ec32b4a6f8a4bd0710eac72`  
		Last Modified: Fri, 12 Jan 2024 19:33:36 GMT  
		Size: 2.6 MB (2598930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42b22c55c8403b8b5ae0a56a7a77313e6ea043ea4210fbda84636bc50852331a`  
		Last Modified: Fri, 12 Jan 2024 19:33:36 GMT  
		Size: 27.2 KB (27245 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bullseye` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:6933f59517fbb9de3bd515537788b6a621e39de17e39d9549efe9a699180549d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55599692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bfff6bfbc6f0e8a890bad9e22c5392e6dbfd67def93467db6231d4be1b719b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e32c7ede661e7251981460fb0412c653a200f957f463492b36af41b74fba8db`  
		Last Modified: Thu, 01 Feb 2024 16:19:23 GMT  
		Size: 25.5 MB (25531605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0fef1260936fd8b00d230c4d2783cad4aeb4a521bed18313e66626073058ed`  
		Last Modified: Thu, 01 Feb 2024 16:19:22 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7ada83d484479440b5bc99136218741950c7c75309daee5afdd8e31edecf3d`  
		Last Modified: Thu, 01 Feb 2024 16:19:22 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c1c6e595590f28de84a77758a0bbd70354252c72bed65071345ee8a201814e`  
		Last Modified: Thu, 01 Feb 2024 16:19:22 GMT  
		Size: 770.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ca97ef7c74cfd965f236a8c62d82d50447c1bc0ac4da87cba236077a80d89d`  
		Last Modified: Thu, 01 Feb 2024 16:19:23 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:ea914b535985fb85fda3c3494a2cdcdeab5de791fc2b81af82e03c2f1e063c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddb8e71638a90db46795f3af88aa2ab4638a56ffa12cfdbe62014106c8f7995`

```dockerfile
```

-	Layers:
	-	`sha256:183a126a54bea4e2de16d067233d7f756fe1a88192c5282995a78985e5ffbf9f`  
		Last Modified: Thu, 01 Feb 2024 16:19:23 GMT  
		Size: 2.6 MB (2588112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c764128217987232f6fa2663eaf0ad763a406abc22b48fb0c2b7c998970bb71`  
		Last Modified: Thu, 01 Feb 2024 16:19:22 GMT  
		Size: 27.2 KB (27173 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bullseye` - linux; 386

```console
$ docker pull nginx@sha256:127c7c4a4974ef1049a964b34a2bc148afa97b87bd0e1f1734ce417c0b7512da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58953190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16d7f582ca10f0d7579b3bd6e034f8be16c997c3f0cb07774968bbc5bf1151c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:0e0961062de8ea0706118b883ee7638aae4465761dec06896f1bd28b9fb4b516 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:854acbf4b2df9e625a11c0e67025dce58b41d948bb7e5d4d5e708e25489f6e8f`  
		Last Modified: Wed, 31 Jan 2024 22:44:37 GMT  
		Size: 32.4 MB (32402507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff88f6ec03faf46bb3757e7ce9a87ff3474c694fee841604c6839e19368054f`  
		Last Modified: Wed, 31 Jan 2024 23:58:10 GMT  
		Size: 26.5 MB (26546936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0265634e3cbd41442a37ce94a666c2d53525816bb09a50e3d43a671af66c8e10`  
		Last Modified: Wed, 31 Jan 2024 23:58:08 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3448832be055d91b833d574ccebe184d2425d44095f9b4934173affeabdb12`  
		Last Modified: Wed, 31 Jan 2024 23:58:08 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b09f63354afb7ee22aa1cb08ac4ade51add0939f0280c4ea05acee479626f5`  
		Last Modified: Wed, 31 Jan 2024 23:58:08 GMT  
		Size: 769.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654e8dbabefc0a901b95e81175d5f4e9adc88c8a37a4ab63c8758bd978aca5a6`  
		Last Modified: Wed, 31 Jan 2024 23:58:09 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:9a126ac2299fb08cd42e489affc840395f20f556abe41cea7bc659b01f6c83a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142521dc5c6449e9f8165a883d3fbc6f24e782118381b4d498bc05389c29c88d`

```dockerfile
```

-	Layers:
	-	`sha256:df2e0fe918df3558690bb29c3d1e06de1a5a82b0f570a458c21024755fbea590`  
		Last Modified: Wed, 31 Jan 2024 23:58:08 GMT  
		Size: 2.6 MB (2593579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3e46cc73af62f612cc513b6e1d1e4a71e0390ab0a5ac325c1a33bf9aafd5608`  
		Last Modified: Wed, 31 Jan 2024 23:58:08 GMT  
		Size: 27.3 KB (27287 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bullseye` - linux; mips64le

```console
$ docker pull nginx@sha256:0dd5aafc00ed0b8b556d07cdfa18ada49ff45cc408ebc643f6420b9dc23b1f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55120815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b37281683d108c66be7a1aab5450ef10947dd3f2debdeaab9a23187ae4dec2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:c74d2ef293040606b9450e82efd37b5ef0dc7ba25160e7762da18e804abd6338 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:231db420c5b3972aa42bcdfd7a71d4d6d22f911ebd5b7ed62d957cef65d0dddf`  
		Last Modified: Wed, 31 Jan 2024 22:39:47 GMT  
		Size: 29.6 MB (29636258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5796be71f0637fe3269da5ac9a6122febf5986ad789623e2c6034d8f07b3d7e0`  
		Last Modified: Thu, 01 Feb 2024 20:59:32 GMT  
		Size: 25.5 MB (25480808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daa55f6e8980d8b77cbae23077ba88e907d3a9fb9695d461bcfebb4b21e73e6`  
		Last Modified: Thu, 01 Feb 2024 20:59:29 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa956583f8be317f9c3e9c49fd15a834c00ecaa39b36e680a0b49e12875e952b`  
		Last Modified: Thu, 01 Feb 2024 20:59:29 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40599f530bf6e3ec0a123d4ce973d752bf619527f2a8b2b1e7bd06c32ca889bf`  
		Last Modified: Thu, 01 Feb 2024 20:59:29 GMT  
		Size: 770.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4efc6720f165ecaa69892c528c81d6be9fab3b9d19fc877b6c18fff07586fd`  
		Last Modified: Thu, 01 Feb 2024 20:59:31 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:c978e3a68db933fad3a441ff32b296e3fdf85eb2be3588ec51e72a80565708f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa719083901c0cf20eba4dbe3b793a7a8f2c0420c79364f6830241c1c3ac94bc`

```dockerfile
```

-	Layers:
	-	`sha256:c0598d51d1311b15eaa7cc1de4e03b5e4cb592cd86ceaf725b5252b78dd38672`  
		Last Modified: Thu, 01 Feb 2024 20:59:29 GMT  
		Size: 27.0 KB (27018 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bullseye` - linux; ppc64le

```console
$ docker pull nginx@sha256:5a5dc31103847fb3dcb7f8117d3f060233ffaa7c5ff5c8a465407cae50f9f864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62769480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1202774923a0d22502e49d506d002ea6329a72451c85595a3d83a18283254caf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:35bb0428da48f0fbc9230db1ecddacb636bc61d82e6701574b518b720ae76d7f in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:4df9a94c24ca5c52fd8a7f1aebc76690845edac56c36acaf79a984722b5e4e48`  
		Last Modified: Wed, 31 Jan 2024 22:35:16 GMT  
		Size: 35.3 MB (35293643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d0f90bffd508c846574bb670edfab48633716d5fcf37cd33468dda88d9d7db`  
		Last Modified: Thu, 01 Feb 2024 13:32:34 GMT  
		Size: 27.5 MB (27472081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e31dd87a69795bcfa2141864963fd918373d88f6a993a8226bf5ac95e89f004`  
		Last Modified: Thu, 01 Feb 2024 13:32:32 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f7094d9fa75c7c16cb98c42aa3d41cbb3f89f50520132c1445d2774e4d3ad5`  
		Last Modified: Thu, 01 Feb 2024 13:32:32 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15c31618c502eb78dcc2f8fd1d012ff95e0da9f0dbcaaa292c4d5d596422c6e`  
		Last Modified: Thu, 01 Feb 2024 13:32:33 GMT  
		Size: 771.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c94f7699e1bed99b1bd1fc0b2e184dfeb0cad972accc535a06dc93982f08d9`  
		Last Modified: Thu, 01 Feb 2024 13:32:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:78e310435252ebf66fd494573faa1bee46bafb866d4e4db42348b0091dbab842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2bb4caec086124cdd6576077ac7bce06cddc1694b2fce3f487e20a26be65f3`

```dockerfile
```

-	Layers:
	-	`sha256:69c08a30b41f22aec64729fa10dfb1ee34dd2fc4f1fce905d5faa4032cdd09b5`  
		Last Modified: Thu, 01 Feb 2024 13:32:33 GMT  
		Size: 2.6 MB (2601167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8895b13fab57471c2eaaa00054906302adb559f3bd7729dd2b9e558e60b2a0d6`  
		Last Modified: Thu, 01 Feb 2024 13:32:33 GMT  
		Size: 27.2 KB (27209 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bullseye` - linux; s390x

```console
$ docker pull nginx@sha256:6e9c33d87fe980d5d865a02ccd49b5d1306b951e201517f98821dc6f1b7cf8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55075240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee5b70073a3db4291b3f7639157e5cc11005c9cd112436398f0d52cb81d8400`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:77a92d4e9397475a6c68f4341baba607a7c875bc6e252de3e096482dd074f8ca in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NJS_VERSION=0.7.12
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1~bullseye
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bullseye nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a8470cec8ee9510bf45556c756635d84eb3cbc0220b52812522196008c6b0d3e`  
		Last Modified: Thu, 11 Jan 2024 01:51:19 GMT  
		Size: 29.7 MB (29656884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d9c5a2f07a4adddb84669c3047a08a7fa467674fc7bf4e6571f686052ba62d`  
		Last Modified: Fri, 12 Jan 2024 10:32:01 GMT  
		Size: 25.4 MB (25414608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01f0c7a0b0307d95439fc0f65145d6ecfaa45f05e378fc0a0e36e2ebaf9a94`  
		Last Modified: Fri, 12 Jan 2024 10:32:01 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062c0917ef1b1c1d7852cb033a90312ffa816a7ec8e5efb653c9568b1cad7f16`  
		Last Modified: Fri, 12 Jan 2024 10:32:01 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c2222e2f2f0d25e9b0dd1f9bd071bc7aae3b0c8071cb793376567c2606e008`  
		Last Modified: Fri, 12 Jan 2024 10:32:01 GMT  
		Size: 769.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69987288394a7aaba0ebc2ee7bfe815d57fc0aa80db50a223a05087565625b6`  
		Last Modified: Fri, 12 Jan 2024 10:32:02 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bullseye` - unknown; unknown

```console
$ docker pull nginx@sha256:b0126e5694fece9ccef91ced064b986492109820409b40102e501e911f231758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2623682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52db815c2de1d6648d268ecb4c358739861f2676c980d895d36c52fac8ce9e0`

```dockerfile
```

-	Layers:
	-	`sha256:4ae1812c53e87e35461d2aa7c1639faa2c12f02ed66678b67dce5d6546fb3fa8`  
		Last Modified: Fri, 12 Jan 2024 10:32:01 GMT  
		Size: 2.6 MB (2596524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3adba536b835ab54a316c24b824ed2371f31852553ecdae7bb14a4a95fe3955e`  
		Last Modified: Fri, 12 Jan 2024 10:32:01 GMT  
		Size: 27.2 KB (27158 bytes)  
		MIME: application/vnd.in-toto+json

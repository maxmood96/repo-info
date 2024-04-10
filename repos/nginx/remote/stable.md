## `nginx:stable`

```console
$ docker pull nginx@sha256:61708e0e98e01d4a890c659724921832f3a2ff04b141fd54d6c642b3131c8863
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

### `nginx:stable` - linux; amd64

```console
$ docker pull nginx@sha256:2e26275ed7a47e8e93f264d39a09ca4bc3f4058c904c75087e237f4ea883f2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57034578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0218f1687660914d2ce279489e9b6d62a5a48d06ab2e27b7710c19d5e904e5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
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
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a1056ea48405cbdf64995d14dc4c4435097c6a28cbf941bd7f524eafe011f3`  
		Last Modified: Wed, 10 Apr 2024 02:54:05 GMT  
		Size: 25.6 MB (25603087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989106bacf00ee358aaf2e9b291a45c3766142d008d02ffe09be6d8efd3d9a7`  
		Last Modified: Wed, 10 Apr 2024 02:54:05 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00d1142b33106cf135e0a082f8be11b233ef95209c59a3f956bad6957072750`  
		Last Modified: Wed, 10 Apr 2024 02:54:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb49393af980543dd9fd2b63dfd65e17d9ebd150a7197a6baed3b62d3c090e27`  
		Last Modified: Wed, 10 Apr 2024 02:54:05 GMT  
		Size: 770.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac1ebd8aebeead2594dc2a466e7eba1c08395263aad4315fd5ee5f40796abea`  
		Last Modified: Wed, 10 Apr 2024 02:54:06 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:c77955a7291b5403d1150279cd591622922803289e57a26f82383bb8d3fb8a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3100961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24f01fe48b67e62787ba62ce0059c17432de01e45a0ff1bd9de1d2b277326c5`

```dockerfile
```

-	Layers:
	-	`sha256:2f39813903ff3c9ef8c515931d5dd26286fbef237c7843d9c0556c75865565ed`  
		Last Modified: Wed, 10 Apr 2024 02:54:05 GMT  
		Size: 3.1 MB (3073635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54247e67c14524aa30ec1d30331c476cacbd49505b3398d9d17a472c26eb1eef`  
		Last Modified: Wed, 10 Apr 2024 02:54:05 GMT  
		Size: 27.3 KB (27326 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm variant v5

```console
$ docker pull nginx@sha256:5059ce33010643f123708edee772734b1dd7114d0c642da00e33cd48e5fe6554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53689256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66b48893088cf7d903203405451308b5c4357ebd4b4533e37053abd77b70dac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:90e7b77db704f73ce102dcbc0f6cbe5d778409a08ca0d29224ab736a76537669 in / 
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
	-	`sha256:5f50de7913c8d45142222ead3575799095853dd5af08b7c42fe0f070c5947afc`  
		Last Modified: Tue, 12 Mar 2024 00:52:28 GMT  
		Size: 28.9 MB (28924563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee34d80a70d02b0a373e792db9b7c1de3e8efc87498144160eb4c94762f39942`  
		Last Modified: Tue, 12 Mar 2024 15:09:58 GMT  
		Size: 24.8 MB (24760936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f35421758d59b7f822103510387e7945f1661530fd01237b3ed1c322b79cb21`  
		Last Modified: Tue, 12 Mar 2024 15:09:57 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc70b39ce7e3694379245cd238943ff261550ff877127029c08174732d9cb4`  
		Last Modified: Tue, 12 Mar 2024 15:09:57 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e12270d47f2e9e510904908425976eeba999f49bf8f95ddc95390164109de8`  
		Last Modified: Tue, 12 Mar 2024 15:09:57 GMT  
		Size: 771.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad47b0006055badac589c21202e5857e7d57701dc394483cc37fd54e3bc3049`  
		Last Modified: Tue, 12 Mar 2024 15:09:58 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:44333ecd8209abe325183638788bedbe43bff41372cd2f5aebaa0f1508ac1f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3111259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945592f2e463adc12094b51b279f3eb0a06b77ee87d7aa2a65c3e78da3a5a082`

```dockerfile
```

-	Layers:
	-	`sha256:40ffc29b900e16afb89b34d81c7f4e421422e98e8d598f46f283a3269ff92fa0`  
		Last Modified: Tue, 12 Mar 2024 15:09:57 GMT  
		Size: 3.1 MB (3084014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7ae585efa3994821716262301d434eb2f60f75484330044e0552102db263c6`  
		Last Modified: Tue, 12 Mar 2024 15:09:57 GMT  
		Size: 27.2 KB (27245 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm variant v7

```console
$ docker pull nginx@sha256:cf08d0269f76ad52b890a1a7cab703a1ee8f033c30c2df394a29eeef2559d742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50467662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e306886f6a0b7641be298bb72fff8e6328f4471cee77ef1f618c91bb8e323b6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:f0436b046c7a5f796efae4d2d2be5a99ad212807e4aa49fc8cc372a4c4c8c4b0 in / 
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
	-	`sha256:5b16029f28c496dabb357a7310d24f957046a925411ccd44eca962c03f85e38e`  
		Last Modified: Tue, 12 Mar 2024 01:04:23 GMT  
		Size: 26.6 MB (26582714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a056fb8b49ba9381a41352ac67918f5782b9357ec4d6c13eff4245293167b0`  
		Last Modified: Wed, 13 Mar 2024 00:55:22 GMT  
		Size: 23.9 MB (23881202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cbd142e320cf09f5764c0d3885e346754ab9c97fd49de5e08f81b7e4462ee1`  
		Last Modified: Wed, 13 Mar 2024 00:55:20 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200c1b642623a23d3b3ddc5b466d0fae317b08c57233a06f7a86b4dcc5bf126f`  
		Last Modified: Wed, 13 Mar 2024 00:55:21 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec9bfdf3a7a630cddcb4cafa6141d7231011de32c426df3a14febfacb429ae9`  
		Last Modified: Wed, 13 Mar 2024 00:55:21 GMT  
		Size: 769.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109cf2485d4c10ec7460ef377344eea3d20299c1ee0f1e1c4d60cfc99d1b1328`  
		Last Modified: Wed, 13 Mar 2024 00:55:22 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:8b73c5ea14222c18a98d42b6df8836876c71c0ef83e84048ddebe13eba3eea74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3113329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85339be61a0aa892cd901a77184f121fa0a41e91e921f4b671fa668b98b5bc78`

```dockerfile
```

-	Layers:
	-	`sha256:655c84043644113dedbb904c3f1038b857c534c0350422d629ef3a7e998dbdd6`  
		Last Modified: Wed, 13 Mar 2024 00:55:21 GMT  
		Size: 3.1 MB (3086084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6593f8b4262a8a8d45483c194da1a74a93394d539481fd555518046a0e2b07d`  
		Last Modified: Wed, 13 Mar 2024 00:55:21 GMT  
		Size: 27.2 KB (27245 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:798b9b09b6e03dd3bacc4f66c24e09c0c9f326d0c35a211e0cb0e32bd378a4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55605420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9d4415537dd79835685ddfb3fdec1efecbf38aada406c280c76cc82afd6a56`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
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
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c71015b009b98a13ce2a6c9b4fe52617d2e9727029a58ea746a10633ecd9d79`  
		Last Modified: Tue, 12 Mar 2024 22:22:30 GMT  
		Size: 25.5 MB (25530555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e7ab0695b68721958909c17221176ccf18c1334939c64ed0d5cb56221916ed`  
		Last Modified: Tue, 12 Mar 2024 22:22:29 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840aa09af8c14573845f41b0394228c346a6a6fc4f9d476f0b08d89f2c4d6ea4`  
		Last Modified: Tue, 12 Mar 2024 22:22:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c67c9feff8c8b30c0778d5dc84608e69d3e6d6c5e909d62c68ce83b3dacf81`  
		Last Modified: Tue, 12 Mar 2024 22:22:29 GMT  
		Size: 769.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599bbeab54f3224427eab34c12e970c0c93eabcd3f857afc9f73217b386162e`  
		Last Modified: Tue, 12 Mar 2024 22:22:30 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:1eee7b2e6c0fd6e5d74e183c6dc8f1afb20e6a7f16bf838f29cc21d35a1f59d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3101061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e905eeabb522c3208084ed2455ba49670218624509920d80fbfb84e8e3a5fe7c`

```dockerfile
```

-	Layers:
	-	`sha256:4f4fba8f060cfa270b1ad032827d21bb164edd1c2f13a2adb617749b7072e46f`  
		Last Modified: Tue, 12 Mar 2024 22:22:30 GMT  
		Size: 3.1 MB (3073888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b4d89fa778c7c3d534a89fa969ea4030ddfee964108af3ba2603541712ca1f`  
		Last Modified: Tue, 12 Mar 2024 22:22:29 GMT  
		Size: 27.2 KB (27173 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; 386

```console
$ docker pull nginx@sha256:c67a2dc9a2cbe1b9aa71482f3dbe2d1a15519bd9d79f148ba6a76eb8858f9e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58956972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7306af98b918cccea53485576f6fdd35a26e0ee24c2a2cdb93222bbc310ec7c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:515cf6a96eea91239bc61e64b973eb555a9299d1053e3c6cb694d8bafa627086 in / 
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
	-	`sha256:4276507bfa4980b432cd9334306e3335cf1bbc8e6dea45aad2ae9ec091223f03`  
		Last Modified: Tue, 12 Mar 2024 01:03:30 GMT  
		Size: 32.4 MB (32407589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3609e7190cb42d97f93a941c845ee207ea7c942adab24765a1e42f7af472b884`  
		Last Modified: Tue, 12 Mar 2024 01:58:28 GMT  
		Size: 26.5 MB (26545627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697f6b054c93e88e7a3201d78c810fc72d38c9cff44c1ee6f6d3594bd3acaf97`  
		Last Modified: Tue, 12 Mar 2024 01:55:18 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa1a44202245b5296df5a05e7eed1d971a1fad8a8ed9101c7ec41478a53ce52`  
		Last Modified: Tue, 12 Mar 2024 01:58:27 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389fa87aa7755590bdf2bc4a1da6d650e1ff3c4c9e338095e947893a53e923a3`  
		Last Modified: Tue, 12 Mar 2024 01:58:27 GMT  
		Size: 771.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b14cf8eb44066234dcf2984b7df5c8e0e3dd738f3411cc8e55e1411d0602fc`  
		Last Modified: Tue, 12 Mar 2024 01:58:28 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:5d6d9b90f6f7460f31290cc893f69550990f947eaf186961793ee122fed5afc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3108020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092664bf4bd6f30a0b0bff921e8f6ada39c6926ada5d540ef2941999a46e6215`

```dockerfile
```

-	Layers:
	-	`sha256:57d66c7c9a91d9031163e9f899b2f518850b72ab41cc4f7713d69ebbb571882c`  
		Last Modified: Tue, 12 Mar 2024 01:58:27 GMT  
		Size: 3.1 MB (3080733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3258d2f5928b5e75256d0477a06049b6045a7634dea4fc8aad5d54a0cd9c7eff`  
		Last Modified: Tue, 12 Mar 2024 01:58:27 GMT  
		Size: 27.3 KB (27287 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; mips64le

```console
$ docker pull nginx@sha256:d5a216e33f071ec77691a1aae165be5bf991f355687d6c095da548813d4bbf70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55122451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06755d064be3f59a0ec40717250fd7d77808395bf8399d898ee848e61d3e5ec7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:a42bb6c1ce6dd3579b82e6f04b91787c20ac276a10c0bc36d42b2b260789343b in / 
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
	-	`sha256:ade123ee9f81df730fd8edfcb3e77a2032d0f4380f0cb466cccda650f64f9560`  
		Last Modified: Tue, 12 Mar 2024 01:18:36 GMT  
		Size: 29.6 MB (29640502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fa2f8ee6b376c2283491cc90557ef42a35ffede1b0f26334caeed5fbc4059d`  
		Last Modified: Wed, 13 Mar 2024 03:19:04 GMT  
		Size: 25.5 MB (25478196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad56488214d3cacab8bfb47980d5a0deec26fd310776fe1ce35250ece59869fe`  
		Last Modified: Wed, 13 Mar 2024 03:19:01 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b507c55a626d4a48134e5aaceb3dca35e886c62cc5fa16f14b09f53e371843d2`  
		Last Modified: Wed, 13 Mar 2024 03:19:01 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a0cf96439b50c6a88754d237b0d9d3d0e695ef90cfc872bb2e524bbcaf2400`  
		Last Modified: Wed, 13 Mar 2024 03:19:01 GMT  
		Size: 770.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4422ba8f01f4c18f2e74d404899b295f7311b91ab25756e7d65cea31515a046b`  
		Last Modified: Wed, 13 Mar 2024 03:19:02 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:d28a08cd0237d295a34aedbf54599d36f289bc26ab02b114cf5dbdc6ee8572e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dd69eb937162f379a7f7d108873825476d468d03d9080343e026fa86417d41`

```dockerfile
```

-	Layers:
	-	`sha256:358b2890b87448d5e8ad259f148da3a94b1e76d5f2b7f24e6016d90b19902d17`  
		Last Modified: Wed, 13 Mar 2024 03:19:01 GMT  
		Size: 27.0 KB (27019 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; ppc64le

```console
$ docker pull nginx@sha256:9718a4bd68bdc393bdae1f21484d4058de1bb908428f75b596c2a84f9b5920e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62772288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a7f8551a395b9cfd63ac4b108c1fd976bb726cfd1f1e4f7811899c2eec77c5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
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
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19316383af1a518adda3c448cb6b9ef1260ccde733220c608a77935f872ca617`  
		Last Modified: Wed, 13 Mar 2024 02:27:24 GMT  
		Size: 27.5 MB (27470525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f90df9fc665681fc2854fe58705990f4aa1597b03daaa0fe98d1da86d918a25`  
		Last Modified: Wed, 13 Mar 2024 02:27:23 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364bf6d72fbdb5f9114007305e72566f5790e8edb5bbbf2a3f81bad304cfd917`  
		Last Modified: Wed, 13 Mar 2024 02:27:23 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624c895c5847a22f4b797160c703359655f985bf36e8a8bea02191cdddcba8e8`  
		Last Modified: Wed, 13 Mar 2024 02:27:23 GMT  
		Size: 771.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1af12cd0305e20ac2f2efddd59b63bb7c9e2129b42bb73e09fc3eac95065b8`  
		Last Modified: Wed, 13 Mar 2024 02:27:24 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:1132b3a0051df433f6ac62c798c5cd7163aba5547fc2c578d3cfef242c299966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3115530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765765d82dfea00bcaa4bd281eaa82f45f37fb5cefc81d67f7f01a756c43d96e`

```dockerfile
```

-	Layers:
	-	`sha256:14060d6ceb20b570d555ff4c40508c8a3d0a15fea37576b3814503bd2df855d8`  
		Last Modified: Wed, 13 Mar 2024 02:27:24 GMT  
		Size: 3.1 MB (3088321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162dfe2a4bc3f56c2d57d1a58bc5d3a88a47f95d57a96bafe1658ded6592d126`  
		Last Modified: Wed, 13 Mar 2024 02:27:23 GMT  
		Size: 27.2 KB (27209 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; s390x

```console
$ docker pull nginx@sha256:76dbd522494760563b1c7c5fc9f1da34b895a2424cd6c6db1b7cae81ee7c70cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55077042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ad589dc4efa56c84fc5dd5d214ef410afaad4dd8311d186c16f2cd8068b28b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:e121f5164f2335792d17befe564e4a4caf1dec33d5039c8245ce418144782215 in / 
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
	-	`sha256:840335d52e6c781c13aaaed8df36659831a5cb0747048da9bf578dd19a02b30e`  
		Last Modified: Tue, 12 Mar 2024 01:21:45 GMT  
		Size: 29.7 MB (29660245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e0c70fe55dc29e77d532e5992b53bd7db9ec03669adb450ac5e200f63ac220`  
		Last Modified: Wed, 13 Mar 2024 16:23:57 GMT  
		Size: 25.4 MB (25413043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8612146575f4469f427e16179322803a0f4bab6d0b8cb98ba416e9338b635e6d`  
		Last Modified: Wed, 13 Mar 2024 16:23:56 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9b3432c07867187432386bb41a5b816ea2e56cbef404e7dcbef539c0cec128`  
		Last Modified: Wed, 13 Mar 2024 16:23:56 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1aa2fbacf87f3557443d5c725f37b71d5f740d8c257d1e29d06db0c9b51a458`  
		Last Modified: Wed, 13 Mar 2024 16:23:56 GMT  
		Size: 770.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba991d458be265bc870a867153af83f0e122c70e305ff4f5c3aa28f894c0c53`  
		Last Modified: Wed, 13 Mar 2024 16:23:57 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:074e43f4e4da7e4e264c39f2ec6d0c84b707ef404dc6180577d5b0e18142fc7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3111049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7a0a3a4fa2f4de0a88bb9fd3a73a625b427bf7ed6395663d144e5841171055`

```dockerfile
```

-	Layers:
	-	`sha256:8b56e549f308493db99502e59fc4dc0d1b443ec26bc61f34a7946fe3cd88612a`  
		Last Modified: Wed, 13 Mar 2024 16:23:56 GMT  
		Size: 3.1 MB (3083890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51b4d032c212d9bbb55c6fe12947e5ae029afad668e5777e0e0ea894d28d0b3`  
		Last Modified: Wed, 13 Mar 2024 16:23:56 GMT  
		Size: 27.2 KB (27159 bytes)  
		MIME: application/vnd.in-toto+json

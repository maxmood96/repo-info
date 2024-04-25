## `nginx:mainline-bookworm`

```console
$ docker pull nginx@sha256:f1f025c6b59fd95ea9423beb3b2a068f0e806a590250c88db74fdc3085252450
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

### `nginx:mainline-bookworm` - linux; amd64

```console
$ docker pull nginx@sha256:4d5a113fd08c4dd57aae6870942f8ab4a7d5fd1594b9749c4ae1b505cfd1e7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70972138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7383c266ef252ad70806f3072ee8e63d2a16d1e6bafa6146a2da867fc7c41759`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 23 Apr 2024 22:15:45 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 22:15:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NGINX_VERSION=1.25.5
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_RELEASE=2~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 22:15:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 22:15:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddb1e6cdf341aca028fb6fc4cbd9c2ba9e9a1cae1b186a587f2dffe33c0d587`  
		Last Modified: Wed, 24 Apr 2024 04:55:27 GMT  
		Size: 41.8 MB (41817076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5252b206aac298fb004dbe62210d127533f8aeb6a5eb0b8f79e28ddc01bd2419`  
		Last Modified: Wed, 24 Apr 2024 04:55:26 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988b92d96970464ab9435aa6af3077e283c1c8eacaee200f8c123315486066ec`  
		Last Modified: Wed, 24 Apr 2024 04:55:26 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7102627a7a6e4da3b80e192b686d57139b8c6d4ff405918dd508e784a4abc639`  
		Last Modified: Wed, 24 Apr 2024 04:55:27 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93295add984dbd114a6f43401f08e6faf4510809e33e8f8a2e6485399fa0e03c`  
		Last Modified: Wed, 24 Apr 2024 04:55:27 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebde0aa1d1aaad9d43da96b7f0e4a4ebccde16cc4d785944629f02406cd54b44`  
		Last Modified: Wed, 24 Apr 2024 04:55:27 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:53395aae589ed0702f1a6491649213b68a32f03d478d8cfb0d6dfd8eb1563fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2938725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12daacca3241307c290864356b88e6fa521a7fd6b8cee13611e6cb4067a0cf2`

```dockerfile
```

-	Layers:
	-	`sha256:031247bc6aa9be14c7b8bcc879231e78d2a9346c0c732ffc95aeb86f334b443a`  
		Last Modified: Wed, 24 Apr 2024 04:55:26 GMT  
		Size: 2.9 MB (2908435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d953d9a2c8fde05f60b7a4011b75d8abdcbfb250e8497a06e559c02d270af3d4`  
		Last Modified: Wed, 24 Apr 2024 04:55:26 GMT  
		Size: 30.3 KB (30290 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; arm variant v5

```console
$ docker pull nginx@sha256:f8f7b3a7023235a68d6a838cb92470fbb39ce0ebd2fb7591b6126d7258df0691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63081038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83694f435ea6c36ae59b24e85c1a5a1068b97526d6a3a8a0c19126cb92c2b568`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Feb 2024 18:24:57 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
# Wed, 14 Feb 2024 18:24:57 GMT
CMD ["bash"]
# Wed, 14 Feb 2024 18:24:57 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Feb 2024 18:24:57 GMT
ENV NGINX_VERSION=1.25.4
# Wed, 14 Feb 2024 18:24:57 GMT
ENV NJS_VERSION=0.8.3
# Wed, 14 Feb 2024 18:24:57 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 14 Feb 2024 18:24:57 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 18:24:57 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Feb 2024 18:24:57 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Feb 2024 18:24:57 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c03f525322300c8cd1792bf5f5b5a0025e599391135fc44cbc8fa011a75154`  
		Last Modified: Wed, 10 Apr 2024 16:36:20 GMT  
		Size: 36.2 MB (36185883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d571658b9b3a3a0d11276a719bad908838975040fd169b28a2dc3f162196445`  
		Last Modified: Wed, 10 Apr 2024 16:36:19 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c9e0df7ca09650c0321d3877cce22544d565ff559ade0d2b8bcacd6552b05b`  
		Last Modified: Wed, 10 Apr 2024 16:36:19 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da560a5e61371e5f5447e3ade69ab5d2792c4500a0fe7a88eb5b094404a70407`  
		Last Modified: Wed, 10 Apr 2024 16:36:19 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc5632bc7fe1bf64ff71cfd8e651bf8ca89c29e0ded698f2b9348e987430a8`  
		Last Modified: Wed, 10 Apr 2024 16:36:20 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6866d2bb7b6e6015506456efeca3b88cc7d10e21f82e6306a0f6f7e54b1ec0`  
		Last Modified: Wed, 10 Apr 2024 16:36:20 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:0f344ba1d500d99d77331a8ca295160214df0017d744943d4e2ce9a9dea03764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c461189c4ae4089a3195703a02598f4e4bd60584c75d0308cc66d6564d66f7c9`

```dockerfile
```

-	Layers:
	-	`sha256:0294387976700a53e181a2dfec5c0e90b870b81af713c58850b67fe960beb05e`  
		Last Modified: Wed, 10 Apr 2024 16:36:19 GMT  
		Size: 2.9 MB (2929064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c0749b32a32275ac2a9aa134cfa62a42587cbd65d3866361bda3c71f496693f`  
		Last Modified: Wed, 10 Apr 2024 16:36:19 GMT  
		Size: 30.2 KB (30176 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; arm variant v7

```console
$ docker pull nginx@sha256:986847e8ce07cafa0415a80ec6985aa89d30d398862512e6ce0112bb53f2c736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59826052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947ad25b1f9c884e65db351b85bd5d60695eda0f500ac97ca082e79be3d1fd74`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 23 Apr 2024 22:15:45 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 22:15:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NGINX_VERSION=1.25.5
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_RELEASE=2~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 22:15:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 22:15:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6af5501db51bfaede87e477d85893fc8d063d7c28d7bc66ba37c573e99db15`  
		Last Modified: Wed, 24 Apr 2024 16:42:27 GMT  
		Size: 35.1 MB (35081011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38a28029808cbf8aac94d04e6d6e1285753f1b307aa8a443c91e1ca593be5ef`  
		Last Modified: Wed, 24 Apr 2024 01:23:29 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72ac0f16541887b79d81743ecbc2b3be2765da2d701d6509b31eed91b900537`  
		Last Modified: Wed, 24 Apr 2024 16:42:25 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0707815c69e2ec946261d6e60cd6b09fe2dc15bb758d6473b992cf8df4246977`  
		Last Modified: Wed, 24 Apr 2024 16:42:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003f32e47b626ad961930e2ae7eb26cedf64d680f24ee624b6f30af2f254cf52`  
		Last Modified: Wed, 24 Apr 2024 16:42:25 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9437463f7db8b0f7176e7788b6b6217fecd4232fed30cfb388d042d120f0b425`  
		Last Modified: Wed, 24 Apr 2024 16:42:26 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:679ba2ed0edca3fa4111df8e30493bdf64184fe028562dd0df5d534a888b0044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c65342206c302497f798cbf6c63a102e03d0dce9328994449451457b2855613`

```dockerfile
```

-	Layers:
	-	`sha256:167f5b59f9d61b7557bc09fb315d6fe1b02f92245bc4bd4fe5e12af2626ba4c4`  
		Last Modified: Wed, 24 Apr 2024 16:42:25 GMT  
		Size: 2.9 MB (2928456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdb329742253fdce715f7a3a2c87798830e6fbf0f34af861d7dff01831269a9c`  
		Last Modified: Wed, 24 Apr 2024 16:42:25 GMT  
		Size: 30.2 KB (30241 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:c45dea554f0f5ff91d08e4f688c0a150b125b55f8be057f8a4498061fb3b86ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67626191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f287221188b5140d04f78a695355bb251cae616639cc86495424c87523fed4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 22:15:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NGINX_VERSION=1.25.5
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_RELEASE=2~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 22:15:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 22:15:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac03684561abc71157296cc49565e44c464a36667376d0518e8fe3d74c3bca5e`  
		Last Modified: Wed, 24 Apr 2024 02:21:39 GMT  
		Size: 38.5 MB (38459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986afc5da1579073a4dfd06291753c109d6560b0da47fa06a7a3aef2144a0d83`  
		Last Modified: Wed, 24 Apr 2024 02:21:38 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35c72682c8a9049997089230757880a44753d068bc57f2e8acd4121a5ed1ef9`  
		Last Modified: Wed, 24 Apr 2024 02:21:38 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba044db9a01368ae169ad3ec27d20935d5308ca98bad27953c2e39496e9bb53`  
		Last Modified: Wed, 24 Apr 2024 02:21:38 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001e6980063403cd9e5ca4b99f0e2ddf82d7e24324d5e93488488aa374e431bc`  
		Last Modified: Wed, 24 Apr 2024 02:21:39 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f173d6f7d22c25ad0049f29d69da7d4a954c9c56e7da6628d2b73cbd8674e061`  
		Last Modified: Wed, 24 Apr 2024 02:21:39 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:a3322a744c3a27f0fd274c3ba622fc4bdf7f0f998421e93d317758ab1ba47c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2938925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e01b95715575493ba1b1f36c988c660d5a24b75e35df442b53837c28ace65`

```dockerfile
```

-	Layers:
	-	`sha256:48e62db0616994bf475c0c3e2f36087975dc516ec1e8b58fce4a175296e36330`  
		Last Modified: Wed, 24 Apr 2024 02:21:39 GMT  
		Size: 2.9 MB (2908780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1baee0b7f712754b8949dfeca3a034807a28932bea030772114d961e12ad94a`  
		Last Modified: Wed, 24 Apr 2024 02:21:37 GMT  
		Size: 30.1 KB (30145 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; 386

```console
$ docker pull nginx@sha256:218723b3b4e3d2a08ceef89a268423cf62f5d79cff8359d1484a021f68decf00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69114630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bad119ecbde86cda1e806cebe063bb4d0c0db2d4d91355cd68414eabf2ad28`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 23 Apr 2024 22:15:45 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 22:15:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NGINX_VERSION=1.25.5
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_RELEASE=2~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 22:15:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 22:15:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b5a62f9e10804fe97b4ecb10e32c25708591d11b51f9b35a642c240584fa7c`  
		Last Modified: Wed, 24 Apr 2024 05:00:33 GMT  
		Size: 38.9 MB (38946858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6cca52429fed0e1c242911e505c468eab13c02a98f717447a70ce1877463ca`  
		Last Modified: Wed, 24 Apr 2024 05:00:32 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14131c0b42c70135de4f14a9eae445090edf8da0952a2f95607935bde24dd6e`  
		Last Modified: Wed, 24 Apr 2024 05:00:32 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89ec0ddd7e70edba465b4567ff1c1d056e4194aa940c0d37583b6a36a625494`  
		Last Modified: Wed, 24 Apr 2024 05:00:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67d6b5f4946ea23326769704cb7bcb784d2a4211b75ac8b2704e8c3b104e0cd`  
		Last Modified: Wed, 24 Apr 2024 05:00:33 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f138c09ed905507cba364619ff58eed9a4a6f297f29cdcfa515f35dcf7af02b2`  
		Last Modified: Wed, 24 Apr 2024 05:00:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:638520cc32479368fe198c41148bfc2d4e1caf3287a565c91e7ceacd92148d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2951840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5adc343a1990d3674374abf2a8e38fe2bc337fd2c1361e5bbc2cf1eb6df2c8c`

```dockerfile
```

-	Layers:
	-	`sha256:3c00230eeab1068414ac057a7c60ce5d8dffec844b78df1054704ea09b88bbe1`  
		Last Modified: Wed, 24 Apr 2024 05:00:32 GMT  
		Size: 2.9 MB (2921609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f338b66321aa8a7e54d2b960b16ae2b18e69d30201b67d49869807da2962ad`  
		Last Modified: Wed, 24 Apr 2024 05:00:32 GMT  
		Size: 30.2 KB (30231 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; mips64le

```console
$ docker pull nginx@sha256:8100305f824f695c0956ab1009698c2c8f73d014d531e773e45878cca038c62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66662216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f7f05123ee65ba48a5854e79a0ebdce0abc2317e621e7de5ab9f9d61159d58`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 23 Apr 2024 22:15:45 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 22:15:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NGINX_VERSION=1.25.5
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_RELEASE=2~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 22:15:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 22:15:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd47abb091108e5221d92c0d5f9998ffd09e2ae4b47280a06cf1af081d887c5`  
		Last Modified: Thu, 25 Apr 2024 00:33:17 GMT  
		Size: 37.5 MB (37513444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d60e37ed4cee37c9a1e66eca6a0fc608a4999cdda86d4bd02670e654255fd2f`  
		Last Modified: Wed, 24 Apr 2024 01:20:02 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdb725c21d70d0a489de5e30a52db86eb1d3c7b5253666608074e5fcbc1f4f2`  
		Last Modified: Thu, 25 Apr 2024 00:33:13 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3010cf6da0be89a860499129695456644df3eaaf3f80ab581f4d50a0654732ca`  
		Last Modified: Thu, 25 Apr 2024 00:33:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb809f0ab8a7fd9ac0e236cb4240ec289eb6c48400ac01596a700c9795f00013`  
		Last Modified: Thu, 25 Apr 2024 00:33:13 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fda5bdffb143c10a56e2b9073ae7f81cd843e97a17c3d16ab9b2368a5582d6`  
		Last Modified: Thu, 25 Apr 2024 00:33:14 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:8f7662bb7b983645c5d47cdff3b9f188946945e76cda4641c2624a871b1ad0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 KB (30015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b46b913b3b0c3f14954ab371059c73423abf70b02abeb6e3fdb03518b7e546`

```dockerfile
```

-	Layers:
	-	`sha256:c8448fd68a84e9dd895a2efc2fb82fdcd972b678ecbd8b8ba566da03943f316e`  
		Last Modified: Thu, 25 Apr 2024 00:33:13 GMT  
		Size: 30.0 KB (30015 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; ppc64le

```console
$ docker pull nginx@sha256:c525c14e853bd4d933d23fabe376e3b3d6f7a139f7c8458300077d6d6caa0fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75435190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbad07166947c79dcae6f1186aae245cd6f0666a26413e28a8b83402875b82e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 23 Apr 2024 22:15:45 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 22:15:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NGINX_VERSION=1.25.5
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_RELEASE=2~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 22:15:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 22:15:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4a8b1e3b0bf2e788a3c106bf00b9530d4a33f8467a99938f56bba1e4f0af1c`  
		Last Modified: Thu, 25 Apr 2024 03:38:08 GMT  
		Size: 42.3 MB (42289393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900875253104383803ebbbea5a4345ea8e2f1260ec81d6b454073ed04e8fbadf`  
		Last Modified: Wed, 24 Apr 2024 01:32:02 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37062f3b6b0b956d8dafb0430e1fe4946d91f4b9a3ab2a6f4754078748d6308`  
		Last Modified: Thu, 25 Apr 2024 03:38:06 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff90a8dd89e9d3ca12cbd44d983bf3ef03e57f8f808f8c955ca06db2703acde`  
		Last Modified: Thu, 25 Apr 2024 03:38:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88cdf74b6ffa84915cd8b835893b4ac28b0560a62f2a3e40f67c494335dcc18a`  
		Last Modified: Thu, 25 Apr 2024 03:38:07 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d791a9be9d713f671731ece98a1823434134c26ce58bb47c806a9c91fe036e93`  
		Last Modified: Thu, 25 Apr 2024 03:38:07 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:e56babad4ee40264251dca5db4ef61523157956ab0f9b153f422f75b13a4673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad6f2546f2f93b535b212fe7ad90deca32bc96960703c5e78d5f8900744f2e5`

```dockerfile
```

-	Layers:
	-	`sha256:c29933234d812e6d937a1fd0883c775a23a6c386cd79d23af2879f40a87e39ff`  
		Last Modified: Thu, 25 Apr 2024 03:38:07 GMT  
		Size: 2.9 MB (2935702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b694a27e5e3f297f710531717a41871f80cf74dc2782e508d27950e20dd816e3`  
		Last Modified: Thu, 25 Apr 2024 03:38:06 GMT  
		Size: 30.2 KB (30197 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; s390x

```console
$ docker pull nginx@sha256:4083eb56b0b5651845aa05154224b947d1492ac140b26440164a5b297febe2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65286274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fafdc98593dbc207c8f166460aa8dc228864c5c005cfdea343bfc8e4a7eba0ee`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 23 Apr 2024 22:15:45 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 22:15:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NGINX_VERSION=1.25.5
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_RELEASE=2~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 22:15:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 22:15:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0865fc00bd9309068d4fbf819af1a93d6b27db11370363c7417ae5dddd42fb79`  
		Last Modified: Thu, 25 Apr 2024 02:40:21 GMT  
		Size: 37.8 MB (37769322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ac85fbe7f26dc4c402b2fdb398d6437fc0f69a879584f34bfb1023f1ce0e1e`  
		Last Modified: Wed, 24 Apr 2024 01:46:45 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9dc2657058d97f0582a19c497ff84ec48f9398ed50439543acfbc31dcfc123`  
		Last Modified: Thu, 25 Apr 2024 02:40:20 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549f655cb41f57fcf9b94e6c469f6af3702588fd51f73863d0334356b22dc72c`  
		Last Modified: Thu, 25 Apr 2024 02:40:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e190321339d9f3b7427b77f55d869b76fe94258cc2f656b0d1a2d4f12e8d3e18`  
		Last Modified: Thu, 25 Apr 2024 02:40:20 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020117174b7a6c72f563a4fe13a02978214b755009be7a8998f204f69c36121`  
		Last Modified: Thu, 25 Apr 2024 02:40:21 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:105efc1e48e65132a812ada1d2a57655f13abfa10844d8bfa6392489d7b84ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2950299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb0cbc7a0a5deb757347b634d9f99ee3a296e7b6305d0f3de5324726a03d99b`

```dockerfile
```

-	Layers:
	-	`sha256:16c9d5e1b831b4c3fb0e3c3dbb2a12ad74bed779c9ed5fb63bd4e1ec6092356b`  
		Last Modified: Thu, 25 Apr 2024 02:40:20 GMT  
		Size: 2.9 MB (2920176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd510fa01f691efeefe59bf8e263d2901bb3e41315d524ef76d6ba07b883e49c`  
		Last Modified: Thu, 25 Apr 2024 02:40:20 GMT  
		Size: 30.1 KB (30123 bytes)  
		MIME: application/vnd.in-toto+json

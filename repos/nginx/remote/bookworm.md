## `nginx:bookworm`

```console
$ docker pull nginx@sha256:07145ce64726c77459474a1e283d45d6755d9b175c2cc0bd85fe693ee09db744
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

### `nginx:bookworm` - linux; amd64

```console
$ docker pull nginx@sha256:cd64407576751d9b9ba4924f758d3d39fe76a6e142c32169625b60934c95f057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70523085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c613f16b664244b150d1c3644cbc387ec1fe8376377f9419992280eb4a82ff3b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Feb 2024 18:24:57 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcdffcd79f0bd371fceec96d609d4cc46b805002a2ea68c74b9d9925dfe5ec2`  
		Last Modified: Wed, 10 Apr 2024 02:54:19 GMT  
		Size: 41.4 MB (41387135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf231d461b3db0da913cf2ab74e989cc3f79ba6d8c23d2bf2fdafd52a177f5a`  
		Last Modified: Wed, 10 Apr 2024 02:54:17 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9590dd9c9881d041113ddd4f1deb5f056e23ecd5bf332b867d4f64a3f648bd2`  
		Last Modified: Wed, 10 Apr 2024 02:54:17 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4033143d8591983af6ede7fca9b1cffcbd3a47f7e149e9cbc5cd0c3047acbf2`  
		Last Modified: Wed, 10 Apr 2024 02:54:18 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abaefc5fcbdecd3accead79308cbc3482a41531d58e0be41c410291dfcf2fd60`  
		Last Modified: Wed, 10 Apr 2024 02:54:19 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcef83155b8b09f1fc20cba2072adf7c02d94e71564e8c68473e47ab4e303fbe`  
		Last Modified: Wed, 10 Apr 2024 02:54:19 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:b2907519ef30fd63d454219c9a12b4afc3ff6f97132dc1139d6570bd87eebde8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2938488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a2eacfc1ddf927b0528216d2ae297778457da028078b80a53734e22e53d46d`

```dockerfile
```

-	Layers:
	-	`sha256:911146ca23833c9b4406a8648313c376e5b404f236accc6ab55b1f71c0bc1fa2`  
		Last Modified: Wed, 10 Apr 2024 02:54:17 GMT  
		Size: 2.9 MB (2908263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c267dae28036cd71eaa00734cf63de42a5780480aad1ce71c0231de3e2bf64a`  
		Last Modified: Wed, 10 Apr 2024 02:54:17 GMT  
		Size: 30.2 KB (30225 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:bookworm` - linux; arm variant v5

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

### `nginx:bookworm` - unknown; unknown

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

### `nginx:bookworm` - linux; arm variant v7

```console
$ docker pull nginx@sha256:d73dc10f5d562127dfc6672ddee8084a908010ad59ec120efca6ee086622553c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59457753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a303c937ca184d34ac044c6efac38ee73044b378c01a73d9b58b7a6b87acab53`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Feb 2024 18:24:57 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
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
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826c5a0e34a33a9f5f1f6d6028fe90da6f257bbfee7f1efcb01c06425a55dd9e`  
		Last Modified: Wed, 13 Mar 2024 00:51:45 GMT  
		Size: 34.7 MB (34736437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5aa3492bf46fe06fdaa0f9ae96fe712fe0ed352b38e43df99287011d58906f`  
		Last Modified: Wed, 13 Mar 2024 00:51:43 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03573142ac470f6f1b51ad5d458740bd5f4a2dd649e55b2cb793b927db083024`  
		Last Modified: Wed, 13 Mar 2024 00:51:43 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82572e74e7faf5c66c94cac4d1be55224b48b1e28bb984b0ea9c80effc42bd1`  
		Last Modified: Wed, 13 Mar 2024 00:51:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdad29d9234be452d9a4f6be1692c1f11258f2a2dc378d6222025ecde4af167`  
		Last Modified: Wed, 13 Mar 2024 00:51:44 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af048b461f9f30dbe502355169ebe1468cc566c58302aff188f4f1f4c0373b0d`  
		Last Modified: Wed, 13 Mar 2024 00:51:44 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:bd85f8aaff184a95d172c67fef72352b416d62a6662899b4bb8bf67b0eaad46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2146c3ae80e43fba38d4d684b4f9741df5103cc45d6df5ee89f2f8c723a5e4d`

```dockerfile
```

-	Layers:
	-	`sha256:de1f153ef700efb9b9fa99c48fdf0ccdcdefc965879c42a031e70b1741cf2722`  
		Last Modified: Wed, 13 Mar 2024 00:51:43 GMT  
		Size: 2.9 MB (2929554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74f4a8dd2741fe0311014a11da3eee1d2fade3f0afc386f2da62521ea4f4089d`  
		Last Modified: Wed, 13 Mar 2024 00:51:43 GMT  
		Size: 30.2 KB (30176 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:bookworm` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:fb6f7ddf4a57af3dc8acd2884def0e3a636ec198c733618e540905b4a1f9b9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67203460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b4217efe5ed7e85a8946668b6adedb8242a5433da2c53273fb4c112f4c5d99`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Feb 2024 18:24:57 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
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
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5745264e68a84af2c5945efbd5caf81208af173edbf7a6a929926598808125ed`  
		Last Modified: Wed, 10 Apr 2024 16:57:13 GMT  
		Size: 38.0 MB (38036718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f07c61775e742da2dff715df99710d9a64c5fe17a30c1bc659a0c0835505d0a`  
		Last Modified: Wed, 10 Apr 2024 16:57:12 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f29c7c07f7a5e2b74888d109fd97e4f1887424a1f112cba400f2fde4ebfb4d`  
		Last Modified: Wed, 10 Apr 2024 16:57:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a639d96fbc1b9b1973b41ad9bd0b45217f1178abff8db319024a655144580ec`  
		Last Modified: Wed, 10 Apr 2024 16:57:12 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba04a51efe12fefb121d32b8361e744b3b8e4021d4ee77b75537062bfd27d09`  
		Last Modified: Wed, 10 Apr 2024 16:57:13 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716495aa6d1850b09291c2b31fc0f1d121affccd17d4e5bc407d3cb1c93703cc`  
		Last Modified: Wed, 10 Apr 2024 16:57:13 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:f0fef4341008c9ab36678675b3b3e0099063c2cc903e901a4ebec93de0cda95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2938686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c326124b3c5967865cc0844aa03c45dae7eb7fb9bd7ae5853e1c1bb87d3c7012`

```dockerfile
```

-	Layers:
	-	`sha256:36508bc1d9be63f44a115ec9c88f04d59742b9735868fc9efba906de9abca207`  
		Last Modified: Wed, 10 Apr 2024 16:57:12 GMT  
		Size: 2.9 MB (2908608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a19abfc154c8e512c2b054baf6561d123a133ba48f17555b4b7806d12696181f`  
		Last Modified: Wed, 10 Apr 2024 16:57:12 GMT  
		Size: 30.1 KB (30078 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:bookworm` - linux; 386

```console
$ docker pull nginx@sha256:0cccf80640270d57f184590427b5ee349aadbb3df40e708b1c3a92b90874a00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68663357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ef83568ccf2bbe40eec4b10ea00f4d8e19b1a7dea7a8d9bd3111ba51165824`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Feb 2024 18:24:57 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8a12324530ee5f84613e96d211626885030160a631737395d95768c92ceec2`  
		Last Modified: Wed, 10 Apr 2024 01:56:30 GMT  
		Size: 38.5 MB (38512257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04fe1a5ed4c779ce6126a7005f21b91b6ecd26cf4ddd0697746bf9f5fb949f8`  
		Last Modified: Wed, 10 Apr 2024 01:56:28 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3168ce8ce604275793b68e5ee223f21fdcb58f450bdf29b32288b15a83f6485e`  
		Last Modified: Wed, 10 Apr 2024 01:56:28 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b61d4b5fbd0f88a92eade5247ab0f71991d91e61bffce02fa629e62d5720539`  
		Last Modified: Wed, 10 Apr 2024 01:56:28 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8557ebf869bc60ff88126b163717d43f942c611d80650679c1930c0571b3bbd`  
		Last Modified: Wed, 10 Apr 2024 01:56:29 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75f63a66f807a7cd95269a4b98b1781eab0ee767f0085a240797fb04a6bae38`  
		Last Modified: Wed, 10 Apr 2024 01:56:30 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:0eb989b01097a3c2f3bd473082c58c2af864906ea338b5f37b3275aa4f12df3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2951603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9548f7a5ded58e045e430481896f3f67832ee90f669f1b05189c74abcc4c04`

```dockerfile
```

-	Layers:
	-	`sha256:a8952647e1632fd128dc1447ccc8f81aaf596fc1f97ea2d425ca2c47af332646`  
		Last Modified: Wed, 10 Apr 2024 01:56:29 GMT  
		Size: 2.9 MB (2921437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8462bdf1bc226014cb6a8ee1ce484838c099fa694fa0767ccd158c98fa081fc`  
		Last Modified: Wed, 10 Apr 2024 01:56:28 GMT  
		Size: 30.2 KB (30166 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:bookworm` - linux; mips64le

```console
$ docker pull nginx@sha256:4454f210ec4dd018ce7a99ffd74ddd361d6d2615de0bfa378a380dbe67e6a756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66170470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615a7686c52e2080b5f33f575c98c2f176c916ae23f8350089263b88fd4eb261`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Feb 2024 18:24:57 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
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
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6663bcb893dfd46f57c07b0d5f64fa8dc6d17415aee8dc680987db3fab1777f`  
		Last Modified: Wed, 13 Mar 2024 03:01:00 GMT  
		Size: 37.0 MB (37046678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bffa148aae8bab73ae2fe34c67c0478f735b3542d7ced1cda1665f86aaff55`  
		Last Modified: Wed, 13 Mar 2024 03:00:56 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ad9ae7311c7b78a2cded75eb419b7413379705cb82d467bb168e2b1f6fdad0`  
		Last Modified: Wed, 13 Mar 2024 03:00:56 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ccd6fc0e61bc1740e4ef63668c95c86306633d97a9c0b030340b6931a80524`  
		Last Modified: Wed, 13 Mar 2024 03:00:56 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75082706885b4f73209527b29dd2831571a38117c41552e0e7fbd33d49b920f`  
		Last Modified: Wed, 13 Mar 2024 03:00:57 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53f1daab7c17e73c864af85c839974ea8a532a89eec69025ffd10a725b3058b`  
		Last Modified: Wed, 13 Mar 2024 03:00:57 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:f034a8b030fc73f8c40413b7b4b13dc87d8ebf4e9cd2bc57206c9e6fa27f3f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 KB (29953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabaf5a4c6e046634cc163faff3db02778e428832117c8f0ce497e155bc1a698`

```dockerfile
```

-	Layers:
	-	`sha256:2c4c148dc09f74c764dffa1398b87fbdbb268cd2f60a5662de886caa4ea78fbf`  
		Last Modified: Wed, 13 Mar 2024 03:00:56 GMT  
		Size: 30.0 KB (29953 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:bookworm` - linux; ppc64le

```console
$ docker pull nginx@sha256:042c5c851dcc9f45e92b028b076f1136b30b8a051a649ec13e97404d4b892842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74905160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adceb5e7bc8b389f7268363f6fbbad00c8dd2833425c2324941a78ccb6cdba79`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Feb 2024 18:24:57 GMT
ADD file:fd6cd6147fc95a907a092392fe95b8ed685d7ed84c60593cd7e9c64a7d574b64 in / 
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
	-	`sha256:4d891dca051cd29ed554a21d46a9f98401d3ae8b7b85da23513e7b4b1e86008c`  
		Last Modified: Wed, 10 Apr 2024 01:31:08 GMT  
		Size: 33.1 MB (33124837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba753177e5e436e31cf27e2333eeca432678b3bd176f78d79aa7149bd68a0be`  
		Last Modified: Wed, 10 Apr 2024 19:27:47 GMT  
		Size: 41.8 MB (41775728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c0cfa1503a748af0e755ec3249e1d6a2e2cee373fe119b725c27084ff62419`  
		Last Modified: Wed, 10 Apr 2024 19:27:45 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1805dce4fb781879c95b8af7eefb491f720a2a13d424ea1ce136ae61bce510a0`  
		Last Modified: Wed, 10 Apr 2024 19:27:45 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d2b2d2b7700ab83d667905ecb6022e15cecc021232ea5945c5bab0ba78ccc4`  
		Last Modified: Wed, 10 Apr 2024 19:27:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568a6ed30a968dc079634757e405a9cf4184b64858d8581bfa04acbdd39e5f9f`  
		Last Modified: Wed, 10 Apr 2024 19:27:46 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93d7c94989b178fa6cd0beaa3dca2cd9c0fbb5f1a10e6b2e70b50e3041ee3d8`  
		Last Modified: Wed, 10 Apr 2024 19:27:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:84676ef20853f9643c7def75e0e504a7b25f07886d18ff60a92c1ba9d75e6d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632420d2e2dbb130b6f0b34e0fba5ab1a90186e07d44d15e858fd984505bfb43`

```dockerfile
```

-	Layers:
	-	`sha256:92bd6b6c49b9fbca3eb5d73e4ffe5bb493e7dce7d1a193a259a60d380fbbe585`  
		Last Modified: Wed, 10 Apr 2024 19:27:46 GMT  
		Size: 2.9 MB (2935526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4049bc5352ec0f531d14394b7e9b4a05a40337dd2d4573c40fa136e689271e69`  
		Last Modified: Wed, 10 Apr 2024 19:27:45 GMT  
		Size: 30.1 KB (30132 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:bookworm` - linux; s390x

```console
$ docker pull nginx@sha256:e4103101260e7894bc037db83eddfeb1cc8e64043cf4ba877a61ea37172e85d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64813514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8945dd458eb425748c7eeca4223036e3c7261f0cf62fff011129036ed42b50bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Feb 2024 18:24:57 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
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
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb32b8abe278672e22c7940b12196d9fd6be8671ff10a72ea323c8a8f65ef2b`  
		Last Modified: Wed, 13 Mar 2024 16:18:14 GMT  
		Size: 37.3 MB (37320236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b2ed80bb6d1a6ff9f969dd4e87ca746b81902abf4c501df122fd2969fcec2b`  
		Last Modified: Wed, 13 Mar 2024 16:18:13 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72fdbb70c2e5a05fc1481ba55045a945adccd13c046a44698d8378b0bef55d4`  
		Last Modified: Wed, 13 Mar 2024 16:18:13 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052b564faadda0134eb72d8bf6fe06690c9e673dd394483060dbd613b5772378`  
		Last Modified: Wed, 13 Mar 2024 16:18:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9708a417ce3e51339327a18f04352e64e63e9094f3965f7c3595089f4e779a54`  
		Last Modified: Wed, 13 Mar 2024 16:18:14 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d62b1e34338f15219a73f2f7e339d62899aca84e6f71b3bfa89e7422bb87a`  
		Last Modified: Wed, 13 Mar 2024 16:18:14 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:e698b8f61e73be5be1431c27e8b2a8cffc127b5f5bff384f6c054b9895c2b063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2951336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff2e918dc313976e23b816874a66ebd8fd3490a90774142f27d5d28da89b5ba`

```dockerfile
```

-	Layers:
	-	`sha256:fc49d210e7eaa792fec42bdd1e8d963901c39fa2d3ea5254d26ea5ed5fc544f4`  
		Last Modified: Wed, 13 Mar 2024 16:18:13 GMT  
		Size: 2.9 MB (2921278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41daf52e0a872ca7a8d88118dd006d51b03c5c74f52ea0b857b4b7a2ccfc6e38`  
		Last Modified: Wed, 13 Mar 2024 16:18:13 GMT  
		Size: 30.1 KB (30058 bytes)  
		MIME: application/vnd.in-toto+json

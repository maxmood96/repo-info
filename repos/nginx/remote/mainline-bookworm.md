## `nginx:mainline-bookworm`

```console
$ docker pull nginx@sha256:9c367186df9a6b18c6735357b8eb7f407347e84aea09beb184961cb83543d46e
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
$ docker pull nginx@sha256:4e02e85a6f060a8406978fa53aafd2d828d0cedf5259275d191bab9afc33249e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70990583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c9858e10ed8be697dc2809db78c57357ffc82de88c69a3dee5d148354679ef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.27.0
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1018f2b8dba8ffec0afc981d5bae673e38ecac6ca29a861d12cccbd820d53f8d`  
		Last Modified: Fri, 21 Jun 2024 19:54:26 GMT  
		Size: 41.8 MB (41835552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b831e78d8e20641c11c527baff6e2c7bae6a43cc1ab4316a5532885d6461b1e7`  
		Last Modified: Fri, 21 Jun 2024 19:54:26 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab22521e91957c19caeb12eadcad2823fdca853477acb38cd5e9a1ebe57e96e`  
		Last Modified: Fri, 21 Jun 2024 19:54:25 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5112bf42775bbb6a896ccd3ad63cbf864976fb1c047a4c56f316cf78d3edd756`  
		Last Modified: Fri, 21 Jun 2024 19:54:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdaf9e4ee2d8507bf2e162c560cfb0b37567db3870235b8940aeb157d628327`  
		Last Modified: Fri, 21 Jun 2024 19:54:26 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06b6fd631e8e2091ce18db1a1b063f14f06a63d0513cafc51500ce7cb1ae2f4`  
		Last Modified: Fri, 21 Jun 2024 19:54:27 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:54ec2db6e1b7c49b1c8a25c3fa36ff20c347bfa02c7a6971591b253d975e097b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2939060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74700998fb5c8a9434f8021990e196fef2b6dc130e103d3ee60ada3496de8dd2`

```dockerfile
```

-	Layers:
	-	`sha256:8bc1daeb87c353ecacf9a695ec693a59f9d8e49e95010e632cb00c69a8a95730`  
		Last Modified: Fri, 21 Jun 2024 19:54:26 GMT  
		Size: 2.9 MB (2908471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ada9d7be63b7cabcdc5e9014c5035bc99472aaf3443ce582c267af61f53fb41`  
		Last Modified: Fri, 21 Jun 2024 19:54:26 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; arm variant v5

```console
$ docker pull nginx@sha256:f8a9263df51cbe028e4820412701b99c0825606895cf202a17ea1261a86868d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63512417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45750ccfe83c78fbd28db21ea47f4f4117b8cf644339f99943793c2714638c75`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:32 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Thu, 13 Jun 2024 00:48:33 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.27.0
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0a45df1808cf6cc9b32839d8835e8549a5f67c10c850425267bc2cee5a8f20`  
		Last Modified: Fri, 21 Jun 2024 20:00:25 GMT  
		Size: 36.6 MB (36597844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ead552efd93ace69ce4928b9136e1f9e29b84511c6d937bf337fb8eaf04657`  
		Last Modified: Fri, 21 Jun 2024 20:00:23 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd36820b8d741536257362152d46668fea79e247a6b80d39535f390fa6b1c5a`  
		Last Modified: Fri, 21 Jun 2024 20:00:23 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7604346d233ebb97e578719f47237e1c07ffbb2b61bf3856ad212760475dfd4e`  
		Last Modified: Fri, 21 Jun 2024 20:00:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a48c3abaa6f9c51b7fb8bb182b523da52b03a57f510e794db9d3b2336136ed`  
		Last Modified: Fri, 21 Jun 2024 20:00:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ac446ea35c92df74d3f37961428661b51520711f0367bb0817eae60e56276b`  
		Last Modified: Fri, 21 Jun 2024 20:00:24 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:3cd70cc6ac273725ced786d2ba1e1c396397fd1d69c9ca3bc48fa5a9db4ace31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b877cdd156b01973d7d4be0e533725fe75156aa8baa53c4ce792dd3bc4286cda`

```dockerfile
```

-	Layers:
	-	`sha256:f655b5519292604c2353857afd1726585264d2611ca4a5e06fd30347f350685e`  
		Last Modified: Fri, 21 Jun 2024 20:00:24 GMT  
		Size: 2.9 MB (2929276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc544e981571eae2847388816ab26cc6c6e8ffc3e009a676737bae0d6d92cf97`  
		Last Modified: Fri, 21 Jun 2024 20:00:23 GMT  
		Size: 30.7 KB (30706 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; arm variant v7

```console
$ docker pull nginx@sha256:9f0c2fb92b8b851ef57edcdf175f17d30fb0312cd22037235481dfc803b5c2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59847330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1759e0b92f1af72d9f9785a0f1662c818374999748df5a9e6b3c64a60edb2f74`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.27.0
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af26d03dcb4cee0cf18f29086195cb43d7de8c78f0a53333922868f04838f3db`  
		Last Modified: Fri, 21 Jun 2024 19:59:45 GMT  
		Size: 35.1 MB (35102512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96a079e2c0af07eeef64b305cf8300ad24a0f2f358981f71248b430dd85b234`  
		Last Modified: Fri, 21 Jun 2024 19:58:13 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed067a4ea17ccce79c76d311c8845ac6ea5821d394d6aeba8db752068d5ec83`  
		Last Modified: Fri, 21 Jun 2024 19:59:44 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e68fa5e70be209ce08962e03326857e1d15de54f2ec70cb6ef2cdc969c62b0`  
		Last Modified: Fri, 21 Jun 2024 19:59:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d169b73b9d0e12c263305da1bedc5a8292fd397a9690935e9999083a9fa7ef`  
		Last Modified: Fri, 21 Jun 2024 19:59:45 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5cdd74cbe7ce8b18dda59a26629a4f723da4bca6ab42b644132be114befad7`  
		Last Modified: Fri, 21 Jun 2024 19:59:45 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:f6c00cab5c3886221869787e17c3fdaec624e1f30385ec71886c4d58d3bc6b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25561dd36ff33c8d1a90e4a674d5fcb54d4ed7cfeec4922fd74142a6ba08e8ec`

```dockerfile
```

-	Layers:
	-	`sha256:db64e72c28e3a574d02092e1a792d84680952ca439fd4951422ee8335b3fa052`  
		Last Modified: Fri, 21 Jun 2024 19:59:44 GMT  
		Size: 2.9 MB (2928492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1ae4f164c390525e5c872a5f0aa3da5e14b86f5a20fdd9e3c9a2cf251276c54`  
		Last Modified: Fri, 21 Jun 2024 19:59:44 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:fb3444ab758aa6b182f6152b9cc7231241911f60e61b928ee53036e4ba2c858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67650104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0469e929ca6320c98871e17260708787ca6e6547a0b4b21a8854e455adac73df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.27.0
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3239ea84a00d153b5b8f81b47548275701d325537ee211a15719a09589e90ec0`  
		Last Modified: Fri, 21 Jun 2024 19:56:17 GMT  
		Size: 38.5 MB (38465834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a8ad130c080c58c8a97ca53a05268959d545b47ea725dafb1da3c25e2ca17d`  
		Last Modified: Fri, 21 Jun 2024 19:56:15 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bd02702dc304158548760ec74963ea4ca7bd0daa383396a9d995b5d2e36e1c`  
		Last Modified: Fri, 21 Jun 2024 19:56:15 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390881360727ed5647282b485cf7cce36ce93ff259fa6ae44040203da6d985e2`  
		Last Modified: Fri, 21 Jun 2024 19:56:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1f7c38d664ca8fe711461ef309ce2285c249cbf742fc78569024e758071efe`  
		Last Modified: Fri, 21 Jun 2024 19:56:16 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6613d6ba458f67ad08079819c8418fa6ed5d630949ece3f3d8eaa0b72edb399e`  
		Last Modified: Fri, 21 Jun 2024 19:56:16 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:f7110bc89ecd35aec18f3347d8db5dfceb6de619f54e0403de0359c02df5cfc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2939891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6df63685b2c64000857a2e31c3944b23249d2fc33abcc9547b8f7d7282685d9`

```dockerfile
```

-	Layers:
	-	`sha256:cf8436b4123f674d1f795182a714bc8873687a1c0982ea8efc6a4547229ce2e8`  
		Last Modified: Fri, 21 Jun 2024 19:56:16 GMT  
		Size: 2.9 MB (2908921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a701c573445db0aca8ce4131e5cd107c004da603ec02e2649727a7d7f71812`  
		Last Modified: Fri, 21 Jun 2024 19:56:15 GMT  
		Size: 31.0 KB (30970 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; 386

```console
$ docker pull nginx@sha256:907f99b7136e45b2438f758a2f7f16fdb22798a53f09dc01d69d5ffde527d5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69144778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745f255da2d328726f6edba3768a49890ba7acecda441aa5583064b58cf257f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 00:38:56 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Thu, 13 Jun 2024 00:38:56 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.27.0
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0a1187ffabf5211412e73c511b93e35806196bd313b33a208be3503badfe44`  
		Last Modified: Fri, 21 Jun 2024 19:59:47 GMT  
		Size: 39.0 MB (38977513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b84073930b86cd6fcfb8ea1708f55475c2bda0cf08f806d89eed24dff25a951`  
		Last Modified: Fri, 21 Jun 2024 19:59:45 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7120ca8c21e75d700cbc9e2d263e88c0193756cb171ce875d03e15af7cf758af`  
		Last Modified: Fri, 21 Jun 2024 19:59:45 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c60cec635c7f49f74a5e3c39e047e2bfb0a71f7774f4c153dad8389b63569c`  
		Last Modified: Fri, 21 Jun 2024 19:59:45 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4f805579c94590e9d2d8c3b578e10bdf73e085951f2aa157fa23089a3b017e`  
		Last Modified: Fri, 21 Jun 2024 19:59:46 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d279bd437cdf80d8022a1b855cd7c8c3b5dc73c766065902ea54ac2cb3d9be`  
		Last Modified: Fri, 21 Jun 2024 19:59:46 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:241a98231e2b53139cf9e8c4304c2351c81c210757ef2500c5d61b50ead2adf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2952175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4846fea4ac940e85ad677a966f241d71abfea8dc3cceea29f59e7e5e02f722`

```dockerfile
```

-	Layers:
	-	`sha256:46909d45d156a9a0bf27dc2a00b3ff323d62f51ad371335f6ddb5f49df465057`  
		Last Modified: Fri, 21 Jun 2024 19:59:45 GMT  
		Size: 2.9 MB (2921645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eeb5f6f57682460248ef20e99f1997cb0f6826a610fe34fc4073ceef2b1c4ee`  
		Last Modified: Fri, 21 Jun 2024 19:59:45 GMT  
		Size: 30.5 KB (30530 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; mips64le

```console
$ docker pull nginx@sha256:d2483ed53d472ae68c8eee1a033e42735d9b84ffb42c3377f45dbba272dfd5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66676512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd95f01d0667d6f27273221f8a161712dd7c94a99dbf858e78f8c68336d8c58d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 01:10:34 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
# Thu, 13 Jun 2024 01:10:39 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.27.0
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eaf8b60e44e1904c0aa72baa9da6a41de5899ae5bfa63803e19bca66d61c3ee`  
		Last Modified: Fri, 21 Jun 2024 20:18:59 GMT  
		Size: 37.5 MB (37528086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3cf8b1b5838e2a5f1d9b6e88de0850a943a8b8442440ac8aa7b00d7be2496d`  
		Last Modified: Fri, 21 Jun 2024 20:18:55 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b372af58c524eb88973419c911ba6b91a5fd06701c46026b3b137eeeab43adc`  
		Last Modified: Fri, 21 Jun 2024 20:18:55 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def98183be87b4d3e24855f8affc0266dfe91a6a4bc7c236139fbb823f426ade`  
		Last Modified: Fri, 21 Jun 2024 20:18:55 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8048c4194b845aee3b256e82f4385baa4ee77476ed780c7c845b6befd4b9398b`  
		Last Modified: Fri, 21 Jun 2024 20:18:56 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f45655bf84b066deaf4e298af78d3fb20e7bddd7dac2bfd3bed6b0c14b96ece`  
		Last Modified: Fri, 21 Jun 2024 20:18:56 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:94aaa6ecbe5d9ea3f533bb82bb6b390c46a889172690746e3721136b05994fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4129d0a17c014dd55162eb43236438014a2d916cb8753f70202926c7391f6f8a`

```dockerfile
```

-	Layers:
	-	`sha256:6d684a3f8e42ceb9c3b92ae2f0dd69ba2b1af17e700cc7c068dda2ed69fbc738`  
		Last Modified: Fri, 21 Jun 2024 20:18:55 GMT  
		Size: 30.4 KB (30439 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; ppc64le

```console
$ docker pull nginx@sha256:2d4beb410010d3b7431d375ab4360d6645e73db5fc6db38b0f6e6a2fbe02e802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75432421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6692b76fcfd711a3483cc315c3fe7af90458ad479e2be88f40d2f2fbd6fce3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:04 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Thu, 13 Jun 2024 01:17:06 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.27.0
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b37fbf96f9f8d1c16bee5828da3e1530b03772ad82b9d4804b5b31e84aebb1`  
		Last Modified: Fri, 21 Jun 2024 20:00:46 GMT  
		Size: 42.3 MB (42286622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4685e338c430fecb5fddf21521f802d54205bd2d93467d2c27c8e77b70fa8fc`  
		Last Modified: Fri, 21 Jun 2024 20:00:44 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb83d74e81f5ab36301192c51625ee7df1b3a15c07372939a0f8023b1f16f12`  
		Last Modified: Fri, 21 Jun 2024 20:00:44 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c40f3bc0fd6d1c68a1e77c3b41a8f56c7699104251836a797272decd2e0e7ec`  
		Last Modified: Fri, 21 Jun 2024 20:00:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241037f8c14728fd22472fa67b817d887b4f8b3c9326f0839fa711a8b182ec5a`  
		Last Modified: Fri, 21 Jun 2024 20:00:45 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e97ba5e2dc3e1af22bf32e8f60017f14a3ed8454f505ebe33cd92e157f6d2fe`  
		Last Modified: Fri, 21 Jun 2024 20:00:46 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:bc652c8fd0f06c1812c6f5429b405ed6d1b2de1f8f3fdd2226d3a86c9281b670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2966401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c65563c4c744d42ab317c76bedc79aaf1d785c51e086c7a39d10df7edd8ae14`

```dockerfile
```

-	Layers:
	-	`sha256:859f4a93e41032bf516627139b995dcdbf36c4fa273221e4de84da29901f1160`  
		Last Modified: Fri, 21 Jun 2024 20:00:45 GMT  
		Size: 2.9 MB (2935738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a90730f7e12145aed0040882abd31f8c09d2c4a0bc80500a06af9da6894b4e7`  
		Last Modified: Fri, 21 Jun 2024 20:00:44 GMT  
		Size: 30.7 KB (30663 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; s390x

```console
$ docker pull nginx@sha256:33f29240f54fc293f2e359e1d690175fa0db4d1b4ce57a8015e1df315681157b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65282845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd3bbcf81e572e25023abb494cd16ebc40119ffcffc16df21175676d1ec8f53`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 00:42:38 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Thu, 13 Jun 2024 00:42:40 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.27.0
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454e4e79d1222472fec2d1456b91d773bd620d432739eb2d246caa4f9cf47703`  
		Last Modified: Fri, 21 Jun 2024 19:58:14 GMT  
		Size: 37.8 MB (37765783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96a079e2c0af07eeef64b305cf8300ad24a0f2f358981f71248b430dd85b234`  
		Last Modified: Fri, 21 Jun 2024 19:58:13 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11e7ab89fd4c823bea15d9af4930e48982d47e4842f7ff005eed60edd9572d3`  
		Last Modified: Fri, 21 Jun 2024 19:58:13 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73986fdb2fd11e09d22162ab7b4b594865c2bcdd4861c73a0ce0018161da446`  
		Last Modified: Fri, 21 Jun 2024 19:58:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04ed5ca36b4072895901264939a1678ebc15e6b1e4d66012f3934a1c218ec5`  
		Last Modified: Fri, 21 Jun 2024 19:58:13 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55b46fe2ed982e2022f72327f183b31d8e71632b4c81125f0f75cefde484922`  
		Last Modified: Fri, 21 Jun 2024 19:58:14 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:40e886e2647f74755ab7f1775d2273a2889510f879f8edc719b8a7d1c2d130f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2950801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940d09f5d1431346b92d6444fa512bb63715203b875f6f72ebb19421fefb8724`

```dockerfile
```

-	Layers:
	-	`sha256:6b648aa972919d494c60dcd1269ee6b21ef53491f714c0005ed0ea672ad8bf74`  
		Last Modified: Fri, 21 Jun 2024 19:58:13 GMT  
		Size: 2.9 MB (2920212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66ed3fa04bc63e8d8a7b29bad96ed78c3bfdce0391537e52f3d5d244c6c83ae6`  
		Last Modified: Fri, 21 Jun 2024 19:58:13 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

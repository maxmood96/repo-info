## `nginx:mainline-bookworm-perl`

```console
$ docker pull nginx@sha256:5840266acc766785e7c552164018292e35abd48592b874b80cae705db0d6849a
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

### `nginx:mainline-bookworm-perl` - linux; amd64

```console
$ docker pull nginx@sha256:bfc63f9ea2a39016e9546ecd64fc5f10e81f30248a05251de133bc308647c5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82125983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6ddd4107924fed1b7290ed3a753e55a015ad9238ee0f2f9937603f5bdb42f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
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
# Wed, 14 Feb 2024 18:24:57 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f6f236f401ac07aa5309d8ade2b0c9d24b9f526bd4e73311bf5c1787cfd49c`  
		Last Modified: Wed, 14 Feb 2024 19:53:49 GMT  
		Size: 41.4 MB (41387085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ea3344e711fd7111dee02f17deebceb725ed1d0ee998f7fb472114dc1399ce`  
		Last Modified: Wed, 14 Feb 2024 19:53:32 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1bb4345a3a849289cfb3e2471c096f374423ec1ef74766137b9de546498612`  
		Last Modified: Wed, 14 Feb 2024 19:53:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8fa4352481b358fc60d40ee20d92da64124d2cf405115640d45980339f47e5`  
		Last Modified: Wed, 14 Feb 2024 19:53:48 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f80e9cdab20387cd09e3c47121ef0eb531043cf0aca1a52aab659de3ccb704`  
		Last Modified: Wed, 14 Feb 2024 19:53:48 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a869624cb60aaa916942dc71c22b194a078dcbbb9b8f54d40512eba55f70b8`  
		Last Modified: Wed, 14 Feb 2024 19:53:49 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d0d5cfeb82271b2a100e7dc45ca3b81472018782a1719a0354b1c568bf0749`  
		Last Modified: Wed, 14 Feb 2024 20:53:02 GMT  
		Size: 11.6 MB (11610219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:72fbe4d89ab0d4ba752dee4ce5cfef8faa2bf38579af9d2b0eda94acd5826994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3bfe45f7cabad3d5f959026f018725961f4e485cf68e2dfd58e74f1608dc27`

```dockerfile
```

-	Layers:
	-	`sha256:7dbebafe2b30386ea14278c86a19b9b6100c23870c96acbd132725017b6ce3aa`  
		Last Modified: Wed, 14 Feb 2024 20:53:01 GMT  
		Size: 3.7 MB (3686081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c316bb13ea93eba0ca8880d5c4197ce0fc364fa65b362035b63669ecdb13a9`  
		Last Modified: Wed, 14 Feb 2024 20:53:01 GMT  
		Size: 24.6 KB (24557 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm-perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:68f2f422e6a598e8ea47e0f655d94b99decce3668de0672bffb4c1c02c92210f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74397911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa7ccd9700bcd5ca73edfa6ad33b5d4886b96af6e6c47603a050e1dc0c3cb32`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:21 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Tue, 13 Feb 2024 01:08:21 GMT
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
# Wed, 14 Feb 2024 18:24:57 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4826396947d32d6bc8d319263dd8151ff9539e795a7facd3bab585a3f1b4d82`  
		Last Modified: Wed, 14 Feb 2024 21:28:05 GMT  
		Size: 36.2 MB (36186169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bec8e72e33518284f83d39153ad1be2ae420d927cc32a24cfd5f9a3ec43b360`  
		Last Modified: Wed, 14 Feb 2024 21:28:03 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f5349442d969762fcbe2317c92bbd1906ff6a4ab07ffef4f7de97ef80b77bb`  
		Last Modified: Wed, 14 Feb 2024 21:28:03 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0575c79fc4b14d89683758552537950b7c6b6a6ea050159d557de449a936ef2b`  
		Last Modified: Wed, 14 Feb 2024 21:28:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda3196ac0b7927a5804a72edf8a76630123013d9226f2892700f33ef5e27705`  
		Last Modified: Wed, 14 Feb 2024 21:28:04 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8888859a56357131026d6361797ab191ce873088387902ce9b0de2ceb00f7cb8`  
		Last Modified: Wed, 14 Feb 2024 21:28:05 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41d851c2541012fd0f2024d78e0a9781b769afd94645b6e07f383177aa59f2e`  
		Last Modified: Wed, 14 Feb 2024 22:11:08 GMT  
		Size: 11.3 MB (11323244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:4689d39628cb35d2b77e81b23fd08bce03347d924ab0acc666ccd97e296e7268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c467f9d73b3bae522f6d4691165f090789edaf149c778c2e2170ff8b73a6b49`

```dockerfile
```

-	Layers:
	-	`sha256:1f4ce8b2b03578c8457f77f8a4da2607c9042c0ec7b6cba68e2b3efe270c5200`  
		Last Modified: Wed, 14 Feb 2024 22:11:08 GMT  
		Size: 3.7 MB (3702807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4142e16ff44c551d29452806e55dd9e876d1e2cddf710965be3034cd0a93e60`  
		Last Modified: Wed, 14 Feb 2024 22:11:07 GMT  
		Size: 24.7 KB (24699 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:abbb69b292fadb68d5c9c4e9cfbbeaaec94c2fd069b41215733768408c1cdb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70601600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de43d43932c5b8363f03805aec95e4723ed1a30bbe391fb837f1289c14e8284`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 24 Oct 2023 22:44:45 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 22:44:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NGINX_VERSION=1.25.3
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NJS_VERSION=0.8.2
# Tue, 24 Oct 2023 22:44:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 24 Oct 2023 22:44:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Oct 2023 22:44:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Oct 2023 22:44:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 24 Oct 2023 22:44:45 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e55ffc699be5e4fa76c18a97f89678629b5312c47ba8778d0541fda0a2bb0a`  
		Last Modified: Sat, 03 Feb 2024 11:49:19 GMT  
		Size: 34.7 MB (34742263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e240582d5e28d879df7518e8ec71d9b25e5191537dd46c2f7b3148d6effb037`  
		Last Modified: Sat, 03 Feb 2024 11:49:17 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811629e8d36782670ee40c4387a9a9d64f803c3be7d126a225a59f83ea7c6ad0`  
		Last Modified: Sat, 03 Feb 2024 11:49:17 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026607ea59da02cac04b15b26e4c398e4109d77845b42bd6552b0a3c0154453b`  
		Last Modified: Sat, 03 Feb 2024 11:49:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d686dab828d4ea54859b7168b3029f2f3fd468a26b288c450b207be1d4956d7`  
		Last Modified: Sat, 03 Feb 2024 11:49:18 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3b2f82a81eb907a5774e737047d22bc638238c53dc5f548dc03ce1b088de6c`  
		Last Modified: Sat, 03 Feb 2024 11:49:18 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66284d19384fcdb4c0722480d9dff199d785b4bbd0acf5fe5ddea0d92f364bd0`  
		Last Modified: Sat, 03 Feb 2024 23:13:29 GMT  
		Size: 11.1 MB (11113206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:fff0f615425221780df1e472475fba2c99e8177548943a228dc27979229a35cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7103d68dc0d104266bcc4dd958ab61959addcbca093536c45cd2bc008befdc5e`

```dockerfile
```

-	Layers:
	-	`sha256:0f8aafc7237f493868d4e41950143bc474c4ef27e1a90349d26f7b32eac7d2d1`  
		Last Modified: Sat, 03 Feb 2024 23:13:29 GMT  
		Size: 3.7 MB (3702847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d6c55f7917028499ca40ff8b13dfbb7ea88f46b449fbb97f55dbca6f30ed6b`  
		Last Modified: Sat, 03 Feb 2024 23:13:28 GMT  
		Size: 24.7 KB (24699 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:c19c391afc2e36d5e74bfe4eaae275a7d6bf81f50165c77068ad03f1351cff38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78761911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce31ea77353f8e4169325a02c6c8614f343e9cb2d9759931dd9ab8fbd50a6a06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
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
# Wed, 14 Feb 2024 18:24:57 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d258780861a60bcc69fa064a1f89af044e1ad02def5c086a8a9e787502571ee`  
		Last Modified: Wed, 14 Feb 2024 22:24:40 GMT  
		Size: 38.0 MB (38036770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d6e9feb830238674896855e02f2a2da922789a46befdccd5c092685daaba0b`  
		Last Modified: Wed, 14 Feb 2024 22:24:39 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e0f9421c7ae0077cf5c799e72856d9d41c5711f09b9fc8462a64dcbea2fe46`  
		Last Modified: Wed, 14 Feb 2024 22:24:39 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a95f763a2f5154199f819a81a107dd7d2fb9172bab210ac0792a1007ffddef`  
		Last Modified: Wed, 14 Feb 2024 22:24:39 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164c21b63fde5458be0dbf2f81e713f81521edee14f8e9d5c8034fd8f37f2770`  
		Last Modified: Wed, 14 Feb 2024 22:24:40 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b452a5fd809b7065e99aad4f80295c2ba1d6000fa9686980164297118eef9e9`  
		Last Modified: Wed, 14 Feb 2024 22:24:40 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1285a4882801986611b806f430e3797d3c0ad406d83f65a6bab4fbf1a74a8896`  
		Last Modified: Wed, 14 Feb 2024 23:30:34 GMT  
		Size: 11.6 MB (11564193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:36bbaf67ce7ba2047f3655f56e776197800a1bedd5889d21aa5389c8d8e18244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c7bc5db04273d4fe3eefb8dd10d6edba6ee4b92e8cdb5ff4e32aef5792c547`

```dockerfile
```

-	Layers:
	-	`sha256:8fa032b59fdde740c6d186977aeedc660ffbea2f6d3f97ad00844b4e76f09450`  
		Last Modified: Wed, 14 Feb 2024 23:30:33 GMT  
		Size: 3.7 MB (3691839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f5a53f5bd5ba7b02980bc5caedc027379cb588e750c0c70f537ee0728ea485`  
		Last Modified: Wed, 14 Feb 2024 23:30:33 GMT  
		Size: 24.6 KB (24603 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm-perl` - linux; 386

```console
$ docker pull nginx@sha256:a33b484e4ad3d8acb63033f15c94f2549377163df12554ef8926d39d76ba9a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80251870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374ce6845470018b8414ea830c28f7492c6fd302b9826527bcc07679785cc739`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
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
# Wed, 14 Feb 2024 18:24:57 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb4d4f4f36b9b023c4617b8cec674e0895fe12892b0a8054772ef0f32a01cb9`  
		Last Modified: Wed, 14 Feb 2024 19:57:41 GMT  
		Size: 38.5 MB (38511237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b748644b1623cad118c1c9e519d59b95598503734e0e02ae8aab519213ef7d`  
		Last Modified: Wed, 14 Feb 2024 19:57:39 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae35280d63d58d31d601cfc8bda538b28d75e9e6289c3559f6e2f034b7148ac9`  
		Last Modified: Wed, 14 Feb 2024 19:57:39 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10623405f870bcc0b893d1e5967fc883b495019bf70be2356ecb8d764793e34`  
		Last Modified: Wed, 14 Feb 2024 19:57:40 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d235459962a7ffcb2cfdf155a718ebc54949d81800edefb92b8aee76cf743ebf`  
		Last Modified: Wed, 14 Feb 2024 19:57:41 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a18c758d88647781e115fd77ae612cb33888d4573360c813701bf86e37c0ea`  
		Last Modified: Wed, 14 Feb 2024 19:57:41 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576e689b8203e49bbec014e0e5102be4486eddb1b3ff5eb0092a068c12269254`  
		Last Modified: Wed, 14 Feb 2024 20:53:37 GMT  
		Size: 11.6 MB (11594236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:d50e58b722b00bb0ac8cb34e79a70b347c18f5d374217853b3525e1539048cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0404f5e21707c6b74c5ead41e61153ce7c061f7d1418d9731e068cc5df0fbcd4`

```dockerfile
```

-	Layers:
	-	`sha256:14a2456a544cfff3a37bd98c055d3871b812ca151487e058cbd815475b133578`  
		Last Modified: Wed, 14 Feb 2024 20:53:36 GMT  
		Size: 3.7 MB (3696244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b16a20fd090e0d162ba437cbcec9224804342cb4f70707e836a186d3eca1516`  
		Last Modified: Wed, 14 Feb 2024 20:53:36 GMT  
		Size: 24.5 KB (24495 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm-perl` - linux; mips64le

```console
$ docker pull nginx@sha256:7687accbe9f20e4941d1fc6b7fa5f99ccef7f181e4167b3f25bcf140f20d6475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77576997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893399930a61ee12594e98343aef72775bb61f9320fed525abecb7b797e1bcd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:14 GMT
ADD file:7b0bbeed7888e49f58bdffd816596bc88b87bd4a3761c5a2590f3123c077899b in / 
# Tue, 13 Feb 2024 02:04:18 GMT
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
# Wed, 14 Feb 2024 18:24:57 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:78ede1ea2c0b185708583060a40bd2aeddee7b533566b4df729e98e5e5de458b`  
		Last Modified: Tue, 13 Feb 2024 02:15:10 GMT  
		Size: 29.1 MB (29119092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9a5f5675a984eab2de39aca9ff168ae328bb59574d0ea0ea557eb1f542c32`  
		Last Modified: Thu, 15 Feb 2024 10:24:24 GMT  
		Size: 37.0 MB (37046766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d56e7594affecbf5254ee29700099cd74c8adbd9187f9d46c61136d3ea31f8`  
		Last Modified: Thu, 15 Feb 2024 10:24:20 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c07ce028e0b24a756d4c90632c17a2d491240b4e6cb831cf64f5e0d1c33381`  
		Last Modified: Thu, 15 Feb 2024 10:24:20 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a68accb929a349544ff04fe0693d6ef20602e77f6d82370f9b094c171977d2`  
		Last Modified: Thu, 15 Feb 2024 10:24:21 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cf8a311a466e4b735006dd9ec16e305d3d2f0228b02f034f799cfb6ddfb4e0`  
		Last Modified: Thu, 15 Feb 2024 10:24:21 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c7f9b7197f5f53a61124f6a7a8e50e0b7e4f570375505e18e242aed5c10d34`  
		Last Modified: Thu, 15 Feb 2024 10:24:21 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0d414e9c0615c41d2ca4a2caf8a364e1201866fd2f4cb7542c5ed153504937`  
		Last Modified: Thu, 15 Feb 2024 11:48:19 GMT  
		Size: 11.4 MB (11406544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:61290485bf150207b14a5e9688f565cef4ecf654207328ce7ec6ebd7fda2ff83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 KB (24480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b9edfd1a4a5235a9904a43958540063f96b376e9ae14058ff06621b4c2d15c`

```dockerfile
```

-	Layers:
	-	`sha256:01f4434a519617c3e123871e95f91d1fd4c26afa71a4befad12696d7a527d823`  
		Last Modified: Thu, 15 Feb 2024 11:48:17 GMT  
		Size: 24.5 KB (24480 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:4680fcc9571db049f8180af85320f754242aac7943ef27d9185c7b2cc5881e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87217803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbadc155aba5a339f5ad0dabcc0bc27d3f455123364c972021b5c5c2b1b17c42`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
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
# Wed, 14 Feb 2024 18:24:57 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc565c139a5299029d1e21f9ca214d2dff8a1f793e1584bef6c02096dd9dc8b`  
		Last Modified: Wed, 14 Feb 2024 20:18:03 GMT  
		Size: 41.8 MB (41776060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453643bf3c559bc0bdcbf8bf6ba0bea12e230e49c7a1f611a56f7ef256127f9b`  
		Last Modified: Wed, 14 Feb 2024 20:18:01 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d6eb2ed37715e385bc3d2ef1ddbf81bfd7284a387153f3d3c7ddb5409191e`  
		Last Modified: Wed, 14 Feb 2024 20:18:01 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2130e9a0d497d204f3cf87b9d847bfa89a22396d307dabf6ed50be3dfdfdcfa1`  
		Last Modified: Wed, 14 Feb 2024 20:18:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cc103bc89749ef0cc19cfbfa6d7d846450fb52c56aec3242de7f1c218b2295`  
		Last Modified: Wed, 14 Feb 2024 20:18:02 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48445d9daaeff81f52aadbe7a85df29cba3fa4073bf83b2dcaec4cbc47f3589f`  
		Last Modified: Wed, 14 Feb 2024 20:18:03 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddbb4fa2830a73324f0f95c4cf823537167a630af890a737b77ce7ab5c01ce`  
		Last Modified: Wed, 14 Feb 2024 21:04:22 GMT  
		Size: 12.3 MB (12318244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:e70ac98dc8b8b326606d76814e996a4710a31fa2b1a47ae1bb32b6be0e7b7370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7b98128b88878569d279dcdeed4e1c9ef7cb0c1398e675c7c0af9978c96807`

```dockerfile
```

-	Layers:
	-	`sha256:0145b3f1cb5bca44011297153a10cc8f3bf7994874d0be0263b27206eaa19783`  
		Last Modified: Wed, 14 Feb 2024 21:04:21 GMT  
		Size: 3.7 MB (3713504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6660ecb301b075a269ea2141dcb3ca4a8779d497d80d62b945ce70ed69190e7f`  
		Last Modified: Wed, 14 Feb 2024 21:04:21 GMT  
		Size: 24.7 KB (24655 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm-perl` - linux; s390x

```console
$ docker pull nginx@sha256:53d486a895ae5da5cab325abe3a086eaeb0a6ab46df9b27436c26f3151d78127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77240084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f70c46441c1d7d4426ce8df3de9bb2df899208c6f4b72adaaf79bda01539813`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 24 Oct 2023 22:44:45 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 22:44:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NGINX_VERSION=1.25.3
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NJS_VERSION=0.8.2
# Tue, 24 Oct 2023 22:44:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 24 Oct 2023 22:44:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Oct 2023 22:44:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Oct 2023 22:44:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 24 Oct 2023 22:44:45 GMT
RUN set -x     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a02b715495a706db90d2b047133591f74cbac3620b71eb3e250d93c6b4c7e24`  
		Last Modified: Tue, 06 Feb 2024 12:21:48 GMT  
		Size: 37.3 MB (37327613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad9f95dd59aa1f7cc8dc9c99700c456fd7cc032c601d991a504cc887bc940eb`  
		Last Modified: Tue, 06 Feb 2024 12:21:48 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4873e0f592aeb4e6420f4f3d2932deb0ef4d8806f7cb7961a51b400d4f1a69ff`  
		Last Modified: Tue, 06 Feb 2024 12:21:48 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44154827e706409505f2bbad61cc1d80072171fd57590bafa1aa713b6a0139c4`  
		Last Modified: Tue, 06 Feb 2024 12:21:47 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51e7ac2201efad5c059dfecddcebd978a11f4a021d3b76efaf9d37913c18d44`  
		Last Modified: Tue, 06 Feb 2024 12:21:48 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b8167bb0db26b6bef1d6f101d3707452750d415410c0048fba5785a299045f`  
		Last Modified: Tue, 06 Feb 2024 12:21:48 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7f08747bf537ddc6d3badf287fd13ee8938efe780b787fc842d49130c259f9`  
		Last Modified: Thu, 08 Feb 2024 18:52:39 GMT  
		Size: 12.4 MB (12394433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:e0317f51c5e54489c098dd2bffeee70fb69fae0d0ba692143846090367ab3a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3719606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472265c218fa66a49794aa377810f88705660e1b0e4e624da65426ed7a840b99`

```dockerfile
```

-	Layers:
	-	`sha256:e548c22661eadbdff28a07748a811a4944d80551b6e90e65fca8fb29eddeffee`  
		Last Modified: Thu, 08 Feb 2024 18:52:39 GMT  
		Size: 3.7 MB (3695031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ba9d3167276bab7f7b169f1534de4167f7ac4b8225595af0265b0a5e6e9c004`  
		Last Modified: Thu, 08 Feb 2024 18:52:39 GMT  
		Size: 24.6 KB (24575 bytes)  
		MIME: application/vnd.in-toto+json

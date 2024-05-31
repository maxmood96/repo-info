## `nginx:stable-bookworm-otel`

```console
$ docker pull nginx@sha256:9361348eb8e2899e2bc80c7d61331e0d28572866e9e163512bc4fa21b0aacaeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:stable-bookworm-otel` - linux; amd64

```console
$ docker pull nginx@sha256:dc4f9df6691e780975af5e1af56c7e68e90498ad45296abd995f70a9dfe0f431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73966004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f2be2870e9a2b81a04695199f2b09c2766d00c710834e0eb83a6f93a748b89`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Wed, 29 May 2024 23:55:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 29 May 2024 23:55:01 GMT
ENV NGINX_VERSION=1.26.1
# Wed, 29 May 2024 23:55:01 GMT
ENV NJS_VERSION=0.8.4
# Wed, 29 May 2024 23:55:01 GMT
ENV NJS_RELEASE=2~bookworm
# Wed, 29 May 2024 23:55:01 GMT
ENV PKG_RELEASE=2~bookworm
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 23:55:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 23:55:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 29 May 2024 23:55:01 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 29 May 2024 23:55:01 GMT
ENV OTEL_VERSION=0.1.0
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-otel             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cd203f28712ac72c307d5adccca5316405deec548246c8ac59b5f3e0217cbb`  
		Last Modified: Thu, 30 May 2024 15:52:39 GMT  
		Size: 41.8 MB (41829255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3addd3eb3dbfb5b3d69303cd4aae75af5164f17e5d0319555c792af67536f9`  
		Last Modified: Thu, 30 May 2024 15:52:38 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2744bd3c38803b771ee0c3e37acf3c6c667922b16672c78e39dc81009aa7078`  
		Last Modified: Thu, 30 May 2024 15:52:38 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c7eef6601a643e3b56eaa2b2208cc5d281f75275fe386f39aa4e085ed9d7cf`  
		Last Modified: Thu, 30 May 2024 15:52:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b362abff7c03531d60b1b7194f36ca0d46049b8913c70955520f5ef88d3eb5e`  
		Last Modified: Thu, 30 May 2024 15:52:39 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e3483e2126a15e588670b1e817ae65b96faad8ba2cca894cb7e8a9196b2212`  
		Last Modified: Thu, 30 May 2024 15:52:39 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6654ce02c79fbbdbe59c57d3ef2634f253cd89ff4e0eef4d3e7ce499cd69d6b3`  
		Last Modified: Thu, 30 May 2024 16:50:12 GMT  
		Size: 3.0 MB (2981740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:abd1d5e62186bd07801f4f74f103e5561cd7d47368553914099924a86c78f1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6338e5b67f75059958c6eeea2d2cf5397f3124d5e66c3400c067a4601ca1ce5`

```dockerfile
```

-	Layers:
	-	`sha256:84d3a997a7d0b219e398e67c73388e33560870f4a530dc88d8e9a287a3f83060`  
		Last Modified: Thu, 30 May 2024 16:50:12 GMT  
		Size: 2.9 MB (2916222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e35828bbd290ca8b77b2e34627350bdeed295f349a34d9a699c83ba44580d19`  
		Last Modified: Thu, 30 May 2024 16:50:12 GMT  
		Size: 19.5 KB (19541 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:a569de50058799b03364d842f3e9f881d08ed8818678503237b6fc63652ac74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70493211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536b45fe44f1b7b5dce4243e1397fd077bb3cce933d5e84b316f6ff86ba07244`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Wed, 29 May 2024 23:55:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 29 May 2024 23:55:01 GMT
ENV NGINX_VERSION=1.26.1
# Wed, 29 May 2024 23:55:01 GMT
ENV NJS_VERSION=0.8.4
# Wed, 29 May 2024 23:55:01 GMT
ENV NJS_RELEASE=2~bookworm
# Wed, 29 May 2024 23:55:01 GMT
ENV PKG_RELEASE=2~bookworm
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 23:55:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 23:55:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 29 May 2024 23:55:01 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 29 May 2024 23:55:01 GMT
ENV OTEL_VERSION=0.1.0
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-otel             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faaa1ff00f11f4ec5bd4d985ade42378aa80c65dc4ac1466ce62e27ba14239c`  
		Last Modified: Thu, 30 May 2024 18:52:33 GMT  
		Size: 38.5 MB (38464041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b0709a9a28f29bfb0618b7832b3e3c1e484112f63a63bc0e69ada9455644e4`  
		Last Modified: Thu, 30 May 2024 18:52:32 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaf9f4d64b0156ced87e0388d0be43a90ca17e173dc00919606d3fc9245fbe0`  
		Last Modified: Thu, 30 May 2024 18:52:32 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6fbeb2590d6a0a6ad301e6d368f22ffed11846939fe356cebbc7c645355b2b`  
		Last Modified: Thu, 30 May 2024 18:52:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743940b4979f795ee05ed44281eeb6dce21bc1c6192589082d2d3f83284e702f`  
		Last Modified: Thu, 30 May 2024 18:52:33 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e6ce11ca329d6251f1b93179c1b09525ade138f8dac9ed7637c28fefde0103`  
		Last Modified: Thu, 30 May 2024 18:52:33 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb4cb346959df977e4d1fb07f2d46d371d54c9dbf1d5cf037b38a3bf3dcfa6f`  
		Last Modified: Thu, 30 May 2024 20:54:28 GMT  
		Size: 2.8 MB (2845065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:b16618b320cd643e25a92fb48324857135ef4b71addf404fbcfe5bc202ebfc55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2936588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385753e3b02172202d27a8c298d431cddfb5ac358c92c690f586d49bcf0ded3c`

```dockerfile
```

-	Layers:
	-	`sha256:126f5aab2ce3d8631fb54ee0f8e5a930fec7ec72ae15d76a8319604061423d65`  
		Last Modified: Thu, 30 May 2024 20:54:28 GMT  
		Size: 2.9 MB (2916625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bafc82923c1f81aaff1492bef23687dd9502672bec9b643fab4d665895f06d14`  
		Last Modified: Thu, 30 May 2024 20:54:28 GMT  
		Size: 20.0 KB (19963 bytes)  
		MIME: application/vnd.in-toto+json

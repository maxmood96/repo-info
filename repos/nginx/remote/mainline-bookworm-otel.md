## `nginx:mainline-bookworm-otel`

```console
$ docker pull nginx@sha256:b8200ab3108e9dbe3f38224cc10658c2e338ad89c736a2ef06a9885acd195abe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:mainline-bookworm-otel` - linux; amd64

```console
$ docker pull nginx@sha256:38f3b9c649699a47c212fd7c519ac8315cd39bb3eb9a24a564720eda2808bb4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73953856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a15f61d90d09e0713bd9859c4458b72f03234e6a61bd890587a7de7e810e51`
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
# Tue, 23 Apr 2024 22:15:45 GMT
ENV OTEL_VERSION=0.1.0
# Tue, 23 Apr 2024 22:15:45 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-otel             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
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
	-	`sha256:7d0fb3a4e6d08349d6e7db60819144205b3ad876d1226a6be892fa536c271b75`  
		Last Modified: Wed, 24 Apr 2024 05:58:15 GMT  
		Size: 3.0 MB (2981718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:029e8bf3ce60dada4496e420d3e0d7db3aeba2cd8db463cb9a301342e144b6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2939306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f661579ebc40f4a2733b5b292cd89b29997f9d89a694ca322167eb1bf2dc5811`

```dockerfile
```

-	Layers:
	-	`sha256:7a5e42c835c9e318f6853c9e4804904ec64afd977374ba5b70b3905eef2c4c33`  
		Last Modified: Wed, 24 Apr 2024 05:58:15 GMT  
		Size: 2.9 MB (2917406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a3abafc186f0f4564b0383072ce627ee903c3ff280a03851f57b51f820f14b`  
		Last Modified: Wed, 24 Apr 2024 05:58:15 GMT  
		Size: 21.9 KB (21900 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:03979f262ad27cbbd46106d66f492f7482c41c64503c95dd415178db51a19a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70471212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfab5d6c45141e0ec602c2ae814575c90af1b39e51b2f44abd570d2e07e1687`
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
# Tue, 23 Apr 2024 22:15:45 GMT
ENV OTEL_VERSION=0.1.0
# Tue, 23 Apr 2024 22:15:45 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-otel             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
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
	-	`sha256:211038e40a4b5e228d9e21e7d050f82ab44644d0d7b8cd86ab75e7899785b404`  
		Last Modified: Wed, 24 Apr 2024 03:14:42 GMT  
		Size: 2.8 MB (2845021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:0422b869e9056535290ea6f35e30de32315e851c67a3d07c0ef305c2a0d7dac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2938600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5f07aabb1f1a2f6bcf01b83a58cb6f6481e82f72bc6bbb5a449ff587e9c6db`

```dockerfile
```

-	Layers:
	-	`sha256:da1ee74f9a8da5a6101ad036741a0452204bc19916e373e11f828b5b1d08aa72`  
		Last Modified: Wed, 24 Apr 2024 03:14:41 GMT  
		Size: 2.9 MB (2917752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6add6aad815df86cabff6b06e7500df569b8bc5f7add60430b48cd95f812fcd2`  
		Last Modified: Wed, 24 Apr 2024 03:14:41 GMT  
		Size: 20.8 KB (20848 bytes)  
		MIME: application/vnd.in-toto+json

## `nginx:1-bookworm`

```console
$ docker pull nginx@sha256:bc5eac5eafc581aeda3008b4b1f07ebba230de2f27d47767129a6a905c84f470
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

### `nginx:1-bookworm` - linux; amd64

```console
$ docker pull nginx@sha256:5341b734e75ce46bbb8e02476434217fd771e23df9a4bfea756a6f3a4a521d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72934168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c8a892f36faf6c9215464005ee6fb8cf0585f70b113c0b030f6cb497a41876`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 02 Oct 2024 17:55:35 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_VERSION=0.8.6
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1039c85176c28c2150dc78c334fede00a9bfd5073b28fd13cccb493ec2a8bd`  
		Last Modified: Tue, 12 Nov 2024 02:03:22 GMT  
		Size: 43.8 MB (43801575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad567d3b8a2ca8d6e3cbd00b3b78feafbb1c7e7e2ce1492648ea01cdd06d50d`  
		Last Modified: Tue, 12 Nov 2024 02:03:03 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c63cd62e4265cc7d1d5f400372335389f0cd0fcb02371a3ad51dd94179417`  
		Last Modified: Tue, 12 Nov 2024 02:03:21 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2712910bdfa8b4178ac3651ab185c2c99cd1caa1e2020dcdfe61da6a6f95d7`  
		Last Modified: Tue, 12 Nov 2024 02:03:21 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0adc47c460195e5b3497d9b36d6952b9d59c04d172e32952dd8e939394bb91`  
		Last Modified: Tue, 12 Nov 2024 02:03:22 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171eebbdf235268f48a1b5778e7fff667b2865120cf48358a83508d190de1000`  
		Last Modified: Tue, 12 Nov 2024 02:03:22 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:3d18ce134907296bdaaa53de206a964c6f685c998578ca12cfcfc158ed940a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2994967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436ade913011ba42a8259adc398db8973e3f34e0c0b7574cc737a209cf3b757f`

```dockerfile
```

-	Layers:
	-	`sha256:3500b89923c954a287084f200679ade67bd595b3d1b5e654d81e7331ab0f6e2e`  
		Last Modified: Tue, 12 Nov 2024 02:03:22 GMT  
		Size: 3.0 MB (2960348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ed937d883ce5b5c94330f8b9322589e18aad1d06bce17f699fcd9395fd52d0`  
		Last Modified: Tue, 12 Nov 2024 02:03:21 GMT  
		Size: 34.6 KB (34619 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; arm variant v5

```console
$ docker pull nginx@sha256:dad3cd2d5e5aa871b98728f1832fac976f6c409a452ce6abee99fe62ef628bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63556323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8731bb9a6ba8d1a4e83e9e35ecd3364afcce1dcaa7e1c77ec93b8fae5ef9df0f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 02 Oct 2024 17:55:35 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_VERSION=0.8.6
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbd3fe23d4cf69893a2fc84446c565f245842fab18caf4a1da85c0ef95ede79`  
		Last Modified: Tue, 12 Nov 2024 02:23:11 GMT  
		Size: 36.7 MB (36661666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6acfedd559119ab17dc7c3dbafe34893be1fb749e97adc0a67e4e2efeaa371b`  
		Last Modified: Tue, 12 Nov 2024 02:23:10 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e4197d32904b11b4f1f2f35c8d7d37ca5b5cf67db087090df67900291fc592`  
		Last Modified: Tue, 12 Nov 2024 02:23:10 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117730a646d1984ac9d621f7e5f0c4a13780993e1208c6b6cb3c26fc3a6e4856`  
		Last Modified: Tue, 12 Nov 2024 02:23:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf751dc1aeb939284b1e938a1b2ab17299f29778d4190112ac6817d9e8b64f1`  
		Last Modified: Tue, 12 Nov 2024 02:23:11 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae75f5af8752b8e2762b13aac21ceeea0a68af18dcb9f8e62cf601da0931b701`  
		Last Modified: Tue, 12 Nov 2024 02:23:11 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:baec0f543a1c91c6e2fb89323a701e9fad98370277d0ff19e9439dd7b8f3c7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3016251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26d315db2d8634a077d1fd2b3bf24f34bedcf1019464d401a402ef34a1ae2cd`

```dockerfile
```

-	Layers:
	-	`sha256:8bd5d536c8359fcfac0d7f1935e546ec2c4e39d4be93428a3774ce084f7457ca`  
		Last Modified: Tue, 12 Nov 2024 02:23:10 GMT  
		Size: 3.0 MB (2981508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339e1ce10dd461be660c7dc7a862d9ef764f13170397ee898e8f758517291686`  
		Last Modified: Tue, 12 Nov 2024 02:23:10 GMT  
		Size: 34.7 KB (34743 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; arm variant v7

```console
$ docker pull nginx@sha256:6e2373f097180bbe3d04658786fcacb5ca0868977ce6ebecbe811dd08d2b6196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61433594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7431a55dfe498095ea1cf33cb7181cfbb7839d38ffe12461c84d45e0c51ac8b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 02 Oct 2024 17:55:35 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_VERSION=0.8.6
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2c9fd0ee13e9708669f2b89d04605d15ad7e49e34bb86573f823412f86ae4b`  
		Last Modified: Tue, 12 Nov 2024 02:55:08 GMT  
		Size: 36.7 MB (36710084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928050e54947b0027df17e3eb8741f10a209125a61da495020c22f20c15e1e55`  
		Last Modified: Tue, 12 Nov 2024 02:55:07 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b0f6373f3e89fa535b5081558d7c7b5864ff80923c9ff21d2deeff13116fe7`  
		Last Modified: Tue, 12 Nov 2024 02:55:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185bbda5dcbab0dd5b6eb6122f2e47c1889b05ef98e1f8b2e0613e09b811f22d`  
		Last Modified: Tue, 12 Nov 2024 02:55:07 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bd729d1ed0a24894bc1c7d30722f5d52e8b3162f526eb608904cbe74b02e91`  
		Last Modified: Tue, 12 Nov 2024 02:55:07 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcaf6ef374c7587e8c54d8f61371dba0cd601bda94d92d968e4db8db2838848`  
		Last Modified: Tue, 12 Nov 2024 02:55:08 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:268865a91a7192589634a3d95e50a36d3d58d1d2e2ea7fd575fe698dda4bf3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2265e678eae2bc6edd3ece18e5aefe650c04aca80d639cde33793d99a0de26b1`

```dockerfile
```

-	Layers:
	-	`sha256:6278804b630bc8b44ca1489ded74b21dd16022908045ee4d4cf910b9bb959e60`  
		Last Modified: Tue, 12 Nov 2024 02:55:07 GMT  
		Size: 3.0 MB (2980475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0062811246a9b0927c27124ca9b3cf5634c7dbafa6ec4f777e05cd05cc72668`  
		Last Modified: Tue, 12 Nov 2024 02:55:06 GMT  
		Size: 34.7 KB (34743 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:bf59355a6d8a42552f258c9ef7327e077309667bbb4d7a410ab891dea95bc3ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69579522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3f95c078122f959979fac556ae6f43746c9f32e5a66526bb503ed1d4adbd07`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 02 Oct 2024 17:55:35 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_VERSION=0.8.6
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6368a7ae7d4114b8cf99df0ecafdcba94eaf8bffb5df31001b4738eae7d929`  
		Last Modified: Tue, 12 Nov 2024 03:26:52 GMT  
		Size: 40.4 MB (40417565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082d73fa4431b591a746b135519656cfb11cee3ca757d8f56000c42b65d33c34`  
		Last Modified: Tue, 12 Nov 2024 03:26:51 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d4c0cc9f6f08c6381eec5e8664fdfe8a2ce854b3230605ce00ca1bf35c1c39`  
		Last Modified: Tue, 12 Nov 2024 03:26:51 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffee2b99561b86e7e03bf0819172806c21c69624fdf1b5fd56273ae52d6608b`  
		Last Modified: Tue, 12 Nov 2024 03:26:51 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81815610209d2f9b04f5a15fd617d8d30974efdbf8e676c1cefee754becc5819`  
		Last Modified: Tue, 12 Nov 2024 03:26:52 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c20fd96d4421f46e1f22bc385514b46b7a0278e8c0cc66ad2d15b20b446946`  
		Last Modified: Tue, 12 Nov 2024 03:26:52 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:356e056f3f2aaaa44b8c7bf9d7a39cbfd10f014605495330f98ff7ace5ef3cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2995593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e0ae83439fc387b389396759d59bf125ff182bd292403fc5290866e1f252ce`

```dockerfile
```

-	Layers:
	-	`sha256:27e02059e4e467ff359451a685461d712d2749e5453225676b709c3c431c350d`  
		Last Modified: Tue, 12 Nov 2024 03:26:51 GMT  
		Size: 3.0 MB (2960798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a724608c426273ce9e1d7fddeffd0bff3aa6d5030f9e5b648802b0bb47158f5f`  
		Last Modified: Tue, 12 Nov 2024 03:26:51 GMT  
		Size: 34.8 KB (34795 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; 386

```console
$ docker pull nginx@sha256:d167c9c1e4e3bbd64897aad0794a253ef85294b4aa2afb8dddbacfd3c25eaa9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71321828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b035fd683bc5514cb773675c4c8ea174e3a58a287701f0306203108251146f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 02 Oct 2024 17:55:35 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_VERSION=0.8.6
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7321e0b26df3d0b2657948bc9b62d853823a1082b7a94164881e6c62ecb7b6`  
		Last Modified: Tue, 12 Nov 2024 02:08:00 GMT  
		Size: 41.2 MB (41171774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5da8a74db8ababad5391b3e9554e16d297f24e89d11068382525b1ee5e3fca2`  
		Last Modified: Tue, 12 Nov 2024 02:07:59 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0cb712e4ff29652b26a17fd350f963cb95de237ca9061247ab727961e3e663`  
		Last Modified: Tue, 12 Nov 2024 02:07:59 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff78ba38b5c1d6f35b58d45bb4e7da9b40839b348931186820e9c83cdc0ff16`  
		Last Modified: Tue, 12 Nov 2024 02:07:59 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7ee66685a2201d62d0050a2291f1a15e118c403ac4841bcd3e513bc890159d`  
		Last Modified: Tue, 12 Nov 2024 02:07:59 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b5100efe4583b0c8048245d8fded2a26d71ddb7a206385d6cecc4b734ea5c3`  
		Last Modified: Tue, 12 Nov 2024 02:07:59 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:c4d3cc574900cfd8aa47e1fee2b7736870bddbde5efadc780feae4813a0e9114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3008185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa9c0602c92556d7d6be5f0b2553443ddbf5bd36fc2a2316380d2852debcce0`

```dockerfile
```

-	Layers:
	-	`sha256:81ed1b71abb0811557803404ffbbed91c10025f343bb72559225a64f73e4fa0d`  
		Last Modified: Tue, 12 Nov 2024 02:07:59 GMT  
		Size: 3.0 MB (2973628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4abefe1428792a0f706946aa2737c2f3f22ac4c4846d1e8b41a7da436f055bc4`  
		Last Modified: Tue, 12 Nov 2024 02:07:59 GMT  
		Size: 34.6 KB (34557 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; mips64le

```console
$ docker pull nginx@sha256:1a01879259f2fe6af6642ef4e60dd2bf75f3ef760a21f3141557763737044268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68753789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0066e2e7ed95ae9d53941f896a7772aa0033a8e96571f61f3e8e4c21ae412e79`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 02 Oct 2024 17:55:35 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_VERSION=0.8.6
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:01c6d0bf10848996e396c89b66742849d41fd852c3610146badf9f612e62945b`  
		Last Modified: Tue, 12 Nov 2024 00:58:28 GMT  
		Size: 29.1 MB (29127365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729e6adc63d12a241a8842cc734c3e35e16a4f9c81299a7919168af64851d22`  
		Last Modified: Tue, 12 Nov 2024 03:27:15 GMT  
		Size: 39.6 MB (39621818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425d4f20eea32dbc93adfe744bbfcb9b7813a63f4981a7970b330886b7865dfc`  
		Last Modified: Tue, 12 Nov 2024 03:27:11 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fc0d5f8d08d28869b071054c2f0ac61c2401fa81a7114c67f4dc59c383af8b`  
		Last Modified: Tue, 12 Nov 2024 03:27:11 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e0d93e8b2cff4a1205678d6aa0855c70f31f3291b979963cd745094e02ed37`  
		Last Modified: Tue, 12 Nov 2024 03:27:11 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b49d4b792cea6d93bf6d6a8c38c0e28f26a14cd57d3241b5d432e5217725bb`  
		Last Modified: Tue, 12 Nov 2024 03:27:12 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c7a9db43bc852929c8eb1d633471dca1985846d5d8d8643d03b1de4d0ce975`  
		Last Modified: Tue, 12 Nov 2024 03:27:12 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:1ecbbdb557e9109914592c17926570240a10141f2bde9c2faf0b7b49fc9f4ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded8088186ebd47bb7750c8478df763aabcdad5d05e39367758ad447a80cf7a4`

```dockerfile
```

-	Layers:
	-	`sha256:45ab4db68a1b9d049873f1fad42ad43f9ae6c7193614cf0d4a203e9a128c8cd6`  
		Last Modified: Tue, 12 Nov 2024 03:27:11 GMT  
		Size: 34.5 KB (34524 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; ppc64le

```console
$ docker pull nginx@sha256:5565a1e8778861472125666ed6afdd40e21b0ca043d28308daaae8c6ab960eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77779542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b85f8aa9a677d07b62e1097e7bc10f1f41b2c1c9f04e0d008ad5bd2ce90d35`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 02 Oct 2024 17:55:35 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_VERSION=0.8.6
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28aff5e4790a2317d51e437477c383414a17042bf36404132a2dca8dc564166`  
		Last Modified: Tue, 12 Nov 2024 03:09:54 GMT  
		Size: 44.6 MB (44649587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52a1542f152d3deb36c279f1b94efab583f290a55fee0d9a1f863a868e99577`  
		Last Modified: Tue, 12 Nov 2024 03:09:49 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbba26c657e2cf70ffcbee1d6651e52019ce3df98c6eae0159ef30292f013b1`  
		Last Modified: Tue, 12 Nov 2024 03:09:49 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa7dcea964f5862268788dfa22a6bbf12850f7107d8756249e1716d21e563af`  
		Last Modified: Tue, 12 Nov 2024 03:09:49 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ded96b2be2a514e9ea1b5c54439a59362dc1aa9f2aaebea477d4f0d9a99039`  
		Last Modified: Tue, 12 Nov 2024 03:09:50 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ef22fa5ba24feedb2fa0d1d8a4308442571243e7cda1145121a8016bc9dc21`  
		Last Modified: Tue, 12 Nov 2024 03:09:50 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:279a2955d3440f56e9e507fbe2fd61876c9ea1175436253585ebb595a3980cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3022812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dea0339cbf404053ef490a0a66f56cfd3e2f0bf1a424be84d7844b38110c948`

```dockerfile
```

-	Layers:
	-	`sha256:443efb3e56c585a7cd93c91147f0a94c0697acda1241bfe451218d1b0f1a23fb`  
		Last Modified: Tue, 12 Nov 2024 03:09:49 GMT  
		Size: 3.0 MB (2988113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e22f99821b5f1085dfe26981fd09ec977e23839319fbcc84ef6e05536ce922e3`  
		Last Modified: Tue, 12 Nov 2024 03:09:49 GMT  
		Size: 34.7 KB (34699 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; s390x

```console
$ docker pull nginx@sha256:e3fa9b73d6d85bba23b9123e4f5500adcd8407a487a98927cdc356d8bebef9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67355234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153c677975e86ff8276f515cadd2aaedd2345c267bec4895863ee624e7ba01da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 02 Oct 2024 17:55:35 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_VERSION=0.8.6
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6ec65b39f7e533d4b27a490f761962e5e05dca4449c3cefb6329301bcd3767`  
		Last Modified: Tue, 12 Nov 2024 03:01:50 GMT  
		Size: 39.9 MB (39859005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a338bc00317861a84f9ef5230905e6b37f1f648a2a69f8b313448c4ea2ab266`  
		Last Modified: Tue, 12 Nov 2024 03:01:49 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a316235553458ad4a4de85dc15c9f6cac12477cea9b4bb42b928403beb0bf4`  
		Last Modified: Tue, 12 Nov 2024 03:01:49 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fef75a1263cc69be6d59be0e2afae36f9090cd0a68723706e55c7a2bfdd7cdb`  
		Last Modified: Tue, 12 Nov 2024 03:01:50 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49f870b8def0ac8d99a91bb5960c534b1f73c14903867c5d908858c51ffa817`  
		Last Modified: Tue, 12 Nov 2024 03:01:50 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dfa1aca96441130c878d1e281cf7e10a78d34856046cf465e74b875c840f0e`  
		Last Modified: Tue, 12 Nov 2024 03:01:50 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:fe84e07050655fa0d1afec71ca48beb4fc0ce72de30c9350d40404af25cbcc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3006315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e3bae02d397c8c06b68178c213985c704601928402d8abbff076cb7c04613d`

```dockerfile
```

-	Layers:
	-	`sha256:3fcb50b42786dce358f164692c883d26756d2c6063cda03d75c773ba89eeb4eb`  
		Last Modified: Tue, 12 Nov 2024 03:01:49 GMT  
		Size: 3.0 MB (2971697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5ea95f4a91165a4d9ed2b2d8a9b064f25dbea36387d62021bc118bc06a3c37`  
		Last Modified: Tue, 12 Nov 2024 03:01:49 GMT  
		Size: 34.6 KB (34618 bytes)  
		MIME: application/vnd.in-toto+json

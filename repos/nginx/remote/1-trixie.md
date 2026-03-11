## `nginx:1-trixie`

```console
$ docker pull nginx@sha256:d0913a153ae2aefba815166d75587667a05773843d8f1726024100cd73462a09
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nginx:1-trixie` - linux; amd64

```console
$ docker pull nginx@sha256:a6bead2c897e9e39ca1a2dbd241f96dc181c8d32adcb6201258624fb37d2c7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62938940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99133eed2307147a04b4ad4a37582c76a9c5c76ae3d9aad90bec0f4b8878d4c0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 22:32:09 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 22:32:09 GMT
ENV NGINX_VERSION=1.29.6
# Tue, 10 Mar 2026 22:32:09 GMT
ENV NJS_VERSION=0.9.6
# Tue, 10 Mar 2026 22:32:09 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:32:09 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 22:32:09 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:32:09 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:32:09 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:32:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 22:32:09 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:32:09 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:32:09 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:32:09 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:32:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 22:32:09 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 22:32:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 22:32:09 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a1d70aee5027b89aeb5eec54823d28982ec97ade2fc5d8837281ecee4dc7af`  
		Last Modified: Tue, 10 Mar 2026 22:32:19 GMT  
		Size: 33.2 MB (33155717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d395129dcefbfb212cd08db7cf1f70d256eefd83c2458c45e18a365b0a5bd0`  
		Last Modified: Tue, 10 Mar 2026 22:32:18 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9da45c1db2401fec7485da87d95235e97e1824cb70c5900fea4fb74a87ba6f`  
		Last Modified: Tue, 10 Mar 2026 22:32:18 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a071c04bd15da01eff3b9f14e784c765ae4e2220ba2041a02d51d55e53e091`  
		Last Modified: Tue, 10 Mar 2026 22:32:18 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79697674b8970919d82181f2856f2494024570b22db3103cc062d6552eccddbd`  
		Last Modified: Tue, 10 Mar 2026 22:32:19 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eef040df109a68da4ee0f20ef79c6a5a3b4942ac19e68422e785632684fcde3`  
		Last Modified: Tue, 10 Mar 2026 22:32:19 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:33564df5f8f5334b28e25be085c93e4251e83398232733f3776506cd40cff297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2852379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61214808975770e4a3b07c2d5a37519c1e86a7959510f4e1e28e1a4ccb67885`

```dockerfile
```

-	Layers:
	-	`sha256:23abb0f9ce55dfc5488fc6045c4edb58ca7369e5dd7f721df501c1d7e7518728`  
		Last Modified: Tue, 10 Mar 2026 22:32:18 GMT  
		Size: 2.8 MB (2817223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99947bc9177029fd2595346665ac75b32350d2ef34808c806d61c28bec94005`  
		Last Modified: Tue, 10 Mar 2026 22:32:18 GMT  
		Size: 35.2 KB (35156 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; arm variant v5

```console
$ docker pull nginx@sha256:d0cfc1dc8a48c60923a8418193fb100f90fbf8adf85c58654cbe82a15d7439ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54150810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffca6828a51736073e95b05d9d8ae2c5059246a4377d2b9d1156a11ae846892`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 22:40:14 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 22:40:14 GMT
ENV NGINX_VERSION=1.29.6
# Tue, 10 Mar 2026 22:40:14 GMT
ENV NJS_VERSION=0.9.6
# Tue, 10 Mar 2026 22:40:14 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:40:14 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 22:40:14 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:40:14 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:40:14 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:40:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 22:40:14 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:40:14 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:40:14 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:40:14 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:40:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 22:40:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 22:40:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 22:40:14 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b6d51020aabff840b2eb7249b67a01bb92b9a2ddd6471fe06a2926b0bbb53b`  
		Last Modified: Tue, 10 Mar 2026 22:40:24 GMT  
		Size: 26.2 MB (26198600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2912e19a591dbb9a2fc44a4b540c3a67d9828becd997fc6663b968931711a5`  
		Last Modified: Tue, 10 Mar 2026 22:40:23 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9cf72f7187c4314323c27f69823304d8e47ab6fb8fce4c8d80de0b31f3a803`  
		Last Modified: Tue, 10 Mar 2026 22:40:23 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed86b568c8c4c30133085db70fe731ffb9028002520387929cc838b32eb79f3`  
		Last Modified: Tue, 10 Mar 2026 22:40:23 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb94bb667595452b45df7e159cdb2c5b2e2b04b237d954832e76356a880899e9`  
		Last Modified: Tue, 10 Mar 2026 22:40:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eebdd46086e79081ebe2bc6d8671789c0870d50cff561e9e7f23843901a41bf`  
		Last Modified: Tue, 10 Mar 2026 22:40:24 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:8657f6654588add913812a2302c2fafc961b04117e5949dc5126340f0b818b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2878647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ae1f6e9a4deb00124c2a015370abc0ca4bfeddc2480180ee5684e1a5633e34`

```dockerfile
```

-	Layers:
	-	`sha256:e392a2b5433eeb68078ee71f0ec2ac6ae009312bb7c5e1299da04e97c84a232d`  
		Last Modified: Tue, 10 Mar 2026 22:40:24 GMT  
		Size: 2.8 MB (2843363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:256fb23366ac3c127cd9fbbc912b53c8ea90b94240dae8ec1801fc289ddfe7d2`  
		Last Modified: Tue, 10 Mar 2026 22:40:23 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; arm variant v7

```console
$ docker pull nginx@sha256:7396dbec59289765cd81327c43ba5c13616acb911bb3d4f25180caea6502641f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52355708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71440e370e23b3ccb42e7d4be840c3155b3ae6675db93f5d08439c1c86f8e5a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 22:39:09 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 22:39:09 GMT
ENV NGINX_VERSION=1.29.6
# Tue, 10 Mar 2026 22:39:09 GMT
ENV NJS_VERSION=0.9.6
# Tue, 10 Mar 2026 22:39:09 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:39:09 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 22:39:09 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:39:09 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:39:09 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:39:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 22:39:09 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:39:09 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:39:09 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:39:09 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:39:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 22:39:09 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 22:39:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 22:39:09 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4881a208eb32e057ddefc552ba65f8d0aead0b49ce19bfc7086dcf46598e8f`  
		Last Modified: Tue, 10 Mar 2026 22:39:18 GMT  
		Size: 26.1 MB (26137359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46b7c5247c85e111be71a41dbc001c20db83d7bc618ad53842d3ad21594b7d1`  
		Last Modified: Tue, 10 Mar 2026 22:39:17 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987dfcb5bdbcdfb2baa59cac16adc1217a42591ae2c54097e14053dc292d4432`  
		Last Modified: Tue, 10 Mar 2026 22:39:17 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913ce8bb089d11ffc44325c5b4e355f322580a617736e9a418d7cbee27f056d9`  
		Last Modified: Tue, 10 Mar 2026 22:39:17 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac559aaeec5933a2665758d9c779f8b03bc9c64a4267fccf1673a7d87badb953`  
		Last Modified: Tue, 10 Mar 2026 22:39:18 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784fa129b04028aeb1a2f2fd85c6a253a8b7208e06ecc3488af7b4f79215c984`  
		Last Modified: Tue, 10 Mar 2026 22:39:18 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:f65d1e352e5cff741bf91374d1fe08d2f7d5cba410f20d849f625d006f61f602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd63b63978aa347064cdae51aad104d407f7b1ce842551a8f71f59d283187e0f`

```dockerfile
```

-	Layers:
	-	`sha256:2a973cbf4ea1231e9fa52b12ed5e23e2d403c4bf57b6bb94efd05b8653f03ca9`  
		Last Modified: Tue, 10 Mar 2026 22:39:17 GMT  
		Size: 2.8 MB (2842108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef9fb29b023560aef9b433c82e96d262b71b633ec191da7628cb1fb585e75b1`  
		Last Modified: Tue, 10 Mar 2026 22:39:17 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:77d544c723c620c6f22cd46e2ccb53a6526142faaace8c0b6ff2a31460e1c880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61280110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8e80999f5f22373b83e0b40afef064017eb1dfc8e27230941b4102803a6ecb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 22:31:32 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 22:31:32 GMT
ENV NGINX_VERSION=1.29.6
# Tue, 10 Mar 2026 22:31:32 GMT
ENV NJS_VERSION=0.9.6
# Tue, 10 Mar 2026 22:31:32 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:31:32 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 22:31:32 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:31:32 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:31:32 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:31:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 22:31:32 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:31:32 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:31:32 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:31:32 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:31:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 22:31:32 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 22:31:32 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 22:31:32 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d456cad1d0ffd44f335e854db0e8f439cc1b88fac173e6c5b0d8257c0f9445dc`  
		Last Modified: Tue, 10 Mar 2026 22:31:43 GMT  
		Size: 31.1 MB (31135414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3a4af256ee6fc4bff2bee866b81a264dd0ff13740db70093d5fbbf2a5beff0`  
		Last Modified: Tue, 10 Mar 2026 22:31:42 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1e80a9149a2eaea6dcca30cf7f254383b8bd83f8d24d3f1797bfcfa9c73a8b`  
		Last Modified: Tue, 10 Mar 2026 22:31:42 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbeac1abb084afc5fd2ab9003e907dd631e70f15318d4f2fd2d53b7e86cf94b1`  
		Last Modified: Tue, 10 Mar 2026 22:31:42 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca7a914ec95a5a2d5a38d6cb878821d75829c56715f7ac2188f8df39c0f4e2a`  
		Last Modified: Tue, 10 Mar 2026 22:31:43 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87363d30ab08f4afcca7ee58f389b775d00944804beadd841dfbee66ad1aa57`  
		Last Modified: Tue, 10 Mar 2026 22:31:43 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:082bde60b7bff329a7db48151d2da26ce44f644277f76587906db9354fb18a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2853038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6bd339e6bd1cd3cb6ced0a83585d6c2936d7f69018a6cef20f52f6c94bf3559`

```dockerfile
```

-	Layers:
	-	`sha256:a50bc5888f624dab586910fb974f4a5bbeb81a536beaafee5f98335d3bc1bfa9`  
		Last Modified: Tue, 10 Mar 2026 22:31:42 GMT  
		Size: 2.8 MB (2817707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91b7c54c9127b66e52499709ff6ccc165e95ab60d93e085078cb6ccceb6c584a`  
		Last Modified: Tue, 10 Mar 2026 22:31:42 GMT  
		Size: 35.3 KB (35331 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; 386

```console
$ docker pull nginx@sha256:bbdb536417b6a60e7329e88c6c5c436aa1c8b6b33f1b1faebc7a7f5013f5aa43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63324059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0423b80e3a722ab9e7cca275216d9f1f50ad3b8de969093c8857d4f9f756c093`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 22:38:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 22:38:08 GMT
ENV NGINX_VERSION=1.29.6
# Tue, 10 Mar 2026 22:38:08 GMT
ENV NJS_VERSION=0.9.6
# Tue, 10 Mar 2026 22:38:08 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:38:08 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 22:38:08 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:38:08 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:38:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:38:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 22:38:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:38:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:38:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:38:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:38:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 22:38:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 22:38:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 22:38:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc48aeb2facb2c9b6e67fc9ddb5f6ed38d3ae74859f61f80ff65014d1bdad1b4`  
		Last Modified: Tue, 10 Mar 2026 22:38:18 GMT  
		Size: 32.0 MB (32025547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e5deeadc28941b70d45efa27a8811153e5e9380f999ae4d82c919bfcc6e357`  
		Last Modified: Tue, 10 Mar 2026 22:38:17 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4355c22a03483ffc5bf83611b444487ecb45de570b06149c3e0dc61a952f89de`  
		Last Modified: Tue, 10 Mar 2026 22:38:17 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4339cb4ff49c7fe0d954822d87d826c5559c16e32f36c8113d04b47db16ecd`  
		Last Modified: Tue, 10 Mar 2026 22:38:17 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21673d89aa1ccb152a890c86f2bc7d06333b9a25d9ed56c6158a45137096ceb6`  
		Last Modified: Tue, 10 Mar 2026 22:38:18 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da9e88671c47379f463dc34a06c514ce371d90d021eb0d673ecf20ceb988477`  
		Last Modified: Tue, 10 Mar 2026 22:38:18 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:9142bc62d72dace2a15116479baf33516c8ed8b503398ec58b714fbd305b4440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8913186ed99c59f9899ad25eeba64c5d3cae2d7017f14cb72d098f15e7f41937`

```dockerfile
```

-	Layers:
	-	`sha256:cdae7ce787cdaac3b4ebb577105ab5a82d08186d97c2fee45a83ed3bb567e914`  
		Last Modified: Tue, 10 Mar 2026 22:38:17 GMT  
		Size: 2.8 MB (2837059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0242e4d9b5b6df3f9b98029d27fc211bc63bc1ae6d8430a44688344769f261`  
		Last Modified: Tue, 10 Mar 2026 22:38:17 GMT  
		Size: 35.1 KB (35094 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; ppc64le

```console
$ docker pull nginx@sha256:d56dc4fbd57f79b0ea9f26559a35bb6932715811f3dff92ac9ac18a669a328fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67088236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec6b0d5de8b885186769239d729611ab442f4290d849db9f7ac909f74d77c4b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 22:43:09 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 22:43:09 GMT
ENV NGINX_VERSION=1.29.6
# Tue, 10 Mar 2026 22:43:09 GMT
ENV NJS_VERSION=0.9.6
# Tue, 10 Mar 2026 22:43:09 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:43:09 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 22:43:09 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:43:09 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:43:09 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:43:10 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 22:43:10 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:43:11 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:43:11 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:43:12 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:43:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 22:43:12 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 22:43:12 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 22:43:12 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a964ce469c4945c89aa1e31d2100d6a6b101ac17344d76a54f67e6840fc6e3fc`  
		Last Modified: Tue, 10 Mar 2026 22:43:33 GMT  
		Size: 33.5 MB (33483422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc3b8cf8221be3004e1d7b9745c885fdc5dce5e8fe900c8bec0bb8caaf00e69`  
		Last Modified: Tue, 10 Mar 2026 22:31:35 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc70630b039e00363c770c66cc10bc347b24e5481884274e335a4414838fbc7`  
		Last Modified: Tue, 10 Mar 2026 22:43:32 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e1bdc399482a5802758e6f9afca49d9c6e4e1b25b6be0881b17eca010e9be3`  
		Last Modified: Tue, 10 Mar 2026 22:43:32 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7e4a7e31f9bfa9555a04742c49130748a45bce062503436d931ae6f068b919`  
		Last Modified: Tue, 10 Mar 2026 22:43:32 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440d1f93b298ae8f1f9f274a1d72156d51a93f58a4a51cc171022e5fb0c8792a`  
		Last Modified: Tue, 10 Mar 2026 22:43:33 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:33244e432546ca45461babc267ba45f8ec17ad2f46b77bc41dfa6164a6fb084b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2879989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d664e4c52767b54b19fbd710072327fbfd757fd4e6e363bd2e06468fc651f0`

```dockerfile
```

-	Layers:
	-	`sha256:a9aaf24e437f72181a83f9c9fe880a510646455f855e912e037a67857de8216c`  
		Last Modified: Tue, 10 Mar 2026 22:43:32 GMT  
		Size: 2.8 MB (2844753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7393c4703ab727a43e371d20a9b2783d813b78c2251a6b60eb5d11353a277c`  
		Last Modified: Tue, 10 Mar 2026 22:43:32 GMT  
		Size: 35.2 KB (35236 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; riscv64

```console
$ docker pull nginx@sha256:d3d3ee5379774d1872e4fdb9f2a06184f05e456bd39afbe7381f32334481b09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57611417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb68f1ebb4fbc9282a064d11889f8b8c54bb6ef33eabb4456d2bc87768a2cd43`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 06:00:39 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 25 Feb 2026 06:00:39 GMT
ENV NGINX_VERSION=1.29.5
# Wed, 25 Feb 2026 06:00:39 GMT
ENV NJS_VERSION=0.9.5
# Wed, 25 Feb 2026 06:00:39 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 25 Feb 2026 06:00:39 GMT
ENV ACME_VERSION=0.3.1
# Wed, 25 Feb 2026 06:00:39 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 25 Feb 2026 06:00:39 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 25 Feb 2026 06:00:39 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 25 Feb 2026 06:00:39 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 25 Feb 2026 06:00:39 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 25 Feb 2026 06:00:39 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 25 Feb 2026 06:00:39 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 25 Feb 2026 06:00:40 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 25 Feb 2026 06:00:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Feb 2026 06:00:40 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Feb 2026 06:00:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Feb 2026 06:00:40 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69861c59b95c20d8a221aff7b4dbfec2c74dde6aed0c0e0245366a6e7c33a1d`  
		Last Modified: Wed, 25 Feb 2026 06:02:10 GMT  
		Size: 29.3 MB (29330398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b00fab1172b9d73b6b47a2cf46ff4fbb809feebdcbce383ea6452ea876aafb`  
		Last Modified: Wed, 25 Feb 2026 06:02:05 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07033ca0e3f64c5812dd1abd8b4358cbef6c3237541d4f4d69a000bacee62b18`  
		Last Modified: Wed, 25 Feb 2026 06:02:05 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f89c5fb920fd68b332a9c61a89be3b2f198692d169f182ca052dab2ec43ae9`  
		Last Modified: Wed, 25 Feb 2026 06:02:05 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e5e32157228f18e91b085287ff4c49b185432172e2beb78bf5e8482a0abb3c`  
		Last Modified: Wed, 25 Feb 2026 06:02:07 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f12e7fecac12875c0591a19f2c763bcac04ea78fdd3c087955506cad79288e`  
		Last Modified: Wed, 25 Feb 2026 06:02:07 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:3a76b67783924ccf7b5f7089cf31886976547e02488db4ab9ac5ca2aab6e875a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f09049cabafe28055d1801d907d44cca46fa690b2e562cd6d754f141edb46ae`

```dockerfile
```

-	Layers:
	-	`sha256:9531c8a57dc009b702d8e096f23024cbc89e54d65bbf13ea486537073bc7ddbb`  
		Last Modified: Wed, 25 Feb 2026 06:02:06 GMT  
		Size: 2.8 MB (2834540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d4f949d8048eb05f85cb8e14ecfca821c2d916616c0a03f5f64a23709fb6af`  
		Last Modified: Wed, 25 Feb 2026 06:02:05 GMT  
		Size: 35.2 KB (35236 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; s390x

```console
$ docker pull nginx@sha256:8838f2a1c99814ef54f52935fe736500e140e475e5fc73e8e9266141c0e6341a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60493744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51d100675667700cdc735146e0e8227ec094c0b6de38d2a4f655c0c1a681851`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 22:37:15 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 22:37:15 GMT
ENV NGINX_VERSION=1.29.6
# Tue, 10 Mar 2026 22:37:15 GMT
ENV NJS_VERSION=0.9.6
# Tue, 10 Mar 2026 22:37:15 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:37:15 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 22:37:15 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:37:15 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:37:15 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:37:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 22:37:16 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:37:16 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:37:16 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:37:16 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:37:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 22:37:16 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 22:37:16 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 22:37:16 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62220cd5208b853f8b299249c21f9c93851688083b8da5c46a87ad5e1f576530`  
		Last Modified: Tue, 10 Mar 2026 22:37:32 GMT  
		Size: 30.7 MB (30650961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3093eef97de6b43d3ec85c59fe9b5fdb3a9c9e83ca81e3ff087ea7c742c26d9`  
		Last Modified: Tue, 10 Mar 2026 22:37:31 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc9d1a72178df50f8e5318edca94787f0d48a78a2558693c21a2da3d63dc16a`  
		Last Modified: Tue, 10 Mar 2026 22:37:31 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980a0d06cb21f3c82799514b4194477c62a1e1b9fa3ef7a021cb4d47fbf02e6`  
		Last Modified: Tue, 10 Mar 2026 22:37:31 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9152c8d0a4cbc56dce264b77f2be14d7b18ae2e4947a335d961e5247f22c49`  
		Last Modified: Tue, 10 Mar 2026 22:37:32 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e61de3bd6593c29e624d74d05cefa0b40ce0e966531dc8f5f6c73bafa8d9f78`  
		Last Modified: Tue, 10 Mar 2026 22:37:32 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:bef67036922bec4e6baa66fe0b2ca6f51506dd4daa79a2b76fbcc07394fb222d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5af7442150dc5a5b5c1f86b3c74c9ce81b56da1661240496e9000c7335ce1c`

```dockerfile
```

-	Layers:
	-	`sha256:585f86fff4b1550023b2e5f54672bb5db8f7950205b75251e0dadf8103573293`  
		Last Modified: Tue, 10 Mar 2026 22:37:31 GMT  
		Size: 2.8 MB (2750509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b94b6d02f200316731d4cd20d8f62b1a03a624670154668f2e951c5f7a56bde9`  
		Last Modified: Tue, 10 Mar 2026 22:37:31 GMT  
		Size: 35.2 KB (35156 bytes)  
		MIME: application/vnd.in-toto+json

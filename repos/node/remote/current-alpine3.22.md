## `node:current-alpine3.22`

```console
$ docker pull node@sha256:31214211871e7c1fed53d111995ec5096f8501697f3206b9e4093202ade151ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `node:current-alpine3.22` - linux; amd64

```console
$ docker pull node@sha256:bef39783ec8998a60adf608e73d56e2bf25d7ca7b68d22cef1fcc24213d62ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57914604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b96ee7e670667d97d24797ca734263bd3c989a0dedc7c721ed348e355df1d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 02 Jul 2025 21:10:14 GMT
ENV NODE_VERSION=24.3.0
# Wed, 02 Jul 2025 21:10:14 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="6426c55f7b2817320d952dd7ea4a2a39ed90157c21eb63a5ff144b6bb9d018ad" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 02 Jul 2025 21:10:14 GMT
ENV YARN_VERSION=1.22.22
# Wed, 02 Jul 2025 21:10:14 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 02 Jul 2025 21:10:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 21:10:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jul 2025 21:10:14 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d88b988b8ad325fdc7461b711ecfd600b41e40e167cb69467f45ee5af2e609`  
		Last Modified: Mon, 07 Jul 2025 20:56:11 GMT  
		Size: 52.9 MB (52856717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1027cac4abcd7bf7357346bde692ed47e8c22916d1fecabdce7d61663c041c5f`  
		Last Modified: Mon, 07 Jul 2025 20:56:04 GMT  
		Size: 1.3 MB (1260594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed002257a6082d0556a5be8690cf2c5c0992cc86668b11a9f8f11ad06dc02554`  
		Last Modified: Mon, 07 Jul 2025 20:56:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-alpine3.22` - unknown; unknown

```console
$ docker pull node@sha256:92c34f935bc47edfd9c0ba75be72cb2b2a59d5996f82cf61ff2108f9bb1fead2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.3 KB (410331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133a49cd833d59f96df9225aaa79a40707e374842e42ae7fcc63f332190ff2a5`

```dockerfile
```

-	Layers:
	-	`sha256:1e70d9361bb626895da37ff8b947b1c4fab02ac49a395918e40377f81b809cce`  
		Last Modified: Mon, 07 Jul 2025 21:40:41 GMT  
		Size: 384.5 KB (384484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4efaaaf89eebb3b6ccd4d37dd3919b17fa788de25f67a4a09e5c503eef37e98`  
		Last Modified: Mon, 07 Jul 2025 21:40:42 GMT  
		Size: 25.8 KB (25847 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull node@sha256:69fcd1838ca97007c0b07ed459a0031a2e5d441218f989171ee2fe3029f4ac11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57627295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9221fb47fc256e4178d515d38fe67efa3d25e679fe50e1219b439d9360afde27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 02:25:22 GMT
ENV NODE_VERSION=24.3.0
# Wed, 25 Jun 2025 02:25:22 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="6426c55f7b2817320d952dd7ea4a2a39ed90157c21eb63a5ff144b6bb9d018ad" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENV YARN_VERSION=1.22.22
# Wed, 25 Jun 2025 02:25:22 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 02:25:22 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d5ed3ba000a0e16ec9d1d086fbd8bba568d66058107ca598c2111d38635742`  
		Last Modified: Wed, 25 Jun 2025 17:33:29 GMT  
		Size: 52.2 MB (52230330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d2d450e1d8b6b449782b3694a26f59d68321cf956c0f7c20435cd1ccead5bc`  
		Last Modified: Wed, 25 Jun 2025 17:33:25 GMT  
		Size: 1.3 MB (1260581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396382e845096db4e49791a4e21b4a805afdb63e109a704473e490696bfb7580`  
		Last Modified: Wed, 25 Jun 2025 17:33:24 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-alpine3.22` - unknown; unknown

```console
$ docker pull node@sha256:30b9dd0f22140e1ed1898378b6787b1a02311cabd0662c4529a4a104bed35201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.2 KB (410222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887ce370bde9745bd2bcd8fb60a3f6e650fb9788fe8c21b60578d79935fc0c58`

```dockerfile
```

-	Layers:
	-	`sha256:b756b559e65ef62813c6882d9e02379947a6536337c5490016cb8ffce2ed0576`  
		Last Modified: Wed, 25 Jun 2025 18:40:38 GMT  
		Size: 384.6 KB (384612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd81f738920e198675783344cc1b7573633e1eb258cdd9217e079a894dd63ac`  
		Last Modified: Wed, 25 Jun 2025 18:40:38 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-alpine3.22` - linux; s390x

```console
$ docker pull node@sha256:5c19ad6e8cd8d80eee89df6a0106d065138d95bc8b1d278d6def89c44e26b690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59196938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa81c4c74d1e9cae5ecdafc2b4b81a4e8488ed9742de52ab0e0d96491a8e4b0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 02:25:22 GMT
ENV NODE_VERSION=24.3.0
# Wed, 25 Jun 2025 02:25:22 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="6426c55f7b2817320d952dd7ea4a2a39ed90157c21eb63a5ff144b6bb9d018ad" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENV YARN_VERSION=1.22.22
# Wed, 25 Jun 2025 02:25:22 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 02:25:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 02:25:22 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d2b89874fc8c2bfbc3cac0dd3848bfea0e4363e5bf1281762325ad8f66dc44`  
		Last Modified: Wed, 25 Jun 2025 22:12:46 GMT  
		Size: 54.3 MB (54288402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c324d203a0a825d1ee0b0d5ad402a06324b04a504df15f58c5663485f798c79f`  
		Last Modified: Wed, 25 Jun 2025 22:12:44 GMT  
		Size: 1.3 MB (1260562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a9a35c27be0cf90a613623fa9eb389ed3183ceb5f533ada37e2da89de7dc58`  
		Last Modified: Wed, 25 Jun 2025 22:12:44 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-alpine3.22` - unknown; unknown

```console
$ docker pull node@sha256:2fcea7b0d9bc0b12048694908122844d2ff6e2dcef3d49951d27deb35697cca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.0 KB (407952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbc548a265e90b8c57467c881cbc2a9a7fdcf7f42cf2f73574e747e70c23aa0`

```dockerfile
```

-	Layers:
	-	`sha256:740b85f2cefc623c2e1c70e641fec6ed5fed9136553ba16e4c4560d6dc96cce4`  
		Last Modified: Thu, 26 Jun 2025 00:39:19 GMT  
		Size: 382.5 KB (382533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de3f64b5f13075bf7a02797a35b1f3db991c6d68fda879bfc9a1eaa358938d2d`  
		Last Modified: Thu, 26 Jun 2025 00:39:19 GMT  
		Size: 25.4 KB (25419 bytes)  
		MIME: application/vnd.in-toto+json

## `node:current-alpine3.23`

```console
$ docker pull node@sha256:fd164609b5ab0c6d49bac138ae06c347e72261ec6ae1de32b6aa9f5ee2271110
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `node:current-alpine3.23` - linux; amd64

```console
$ docker pull node@sha256:cbbf2042556f72c8a533313dbb645dd0ec125394651129a3817118022c8efb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57294306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dde43198fbd298e161d9d50413c9ac55f50b3eb1b8973f975fbc8997134f58d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 21:12:23 GMT
ENV NODE_VERSION=25.2.1
# Thu, 04 Dec 2025 21:12:23 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="2cacd704a60accb358852fd565ae85ef83bd368578037bf936b8597ce2935773" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 04 Dec 2025 21:12:23 GMT
ENV YARN_VERSION=1.22.22
# Thu, 04 Dec 2025 21:12:26 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 04 Dec 2025 21:12:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 21:12:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 21:12:26 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6144cdf1ae36dd3ee518f2091b4a467f9e313777a94910f23252a7f0d1e986`  
		Last Modified: Thu, 04 Dec 2025 21:12:55 GMT  
		Size: 52.2 MB (52172446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54f8943466cf9aa9ac530052aef8616c46148ffc9df22839ac4201efaea393d`  
		Last Modified: Thu, 04 Dec 2025 21:12:52 GMT  
		Size: 1.3 MB (1262098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5572ab4bb22b0fe173df3cc7cca964b150e54f4bcaa67cf5a5f1f8eff4b2778`  
		Last Modified: Thu, 04 Dec 2025 21:12:51 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-alpine3.23` - unknown; unknown

```console
$ docker pull node@sha256:c1decb296b2511f1a4eaea50ec98f3df1300b15d3b927323a4982407fbd34ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 KB (398683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba3895d4c036917d92891785fad57c8ffded312e44ebb221069b10814072f7c`

```dockerfile
```

-	Layers:
	-	`sha256:001079f19856cf62f09ca62a1d47045a9fcbe5d57ea9212b13ea8c08f305b4f2`  
		Last Modified: Thu, 04 Dec 2025 22:42:32 GMT  
		Size: 372.9 KB (372879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d3ef5bbc242598ae5cd870d5b9503b57a75c88995b88c0748430671b9483ef4`  
		Last Modified: Thu, 04 Dec 2025 22:42:33 GMT  
		Size: 25.8 KB (25804 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull node@sha256:0495a5e8a1acb237acc0a0b5ce11b6b107cb1c260b3e611470fb1cb667f39c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58595705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f034f75ffb71c21625e3ab89196f59de9bfb30e742ef3795bf4e269285c5d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 21:48:48 GMT
ENV NODE_VERSION=25.2.1
# Thu, 04 Dec 2025 21:48:48 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="2cacd704a60accb358852fd565ae85ef83bd368578037bf936b8597ce2935773" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 04 Dec 2025 21:48:48 GMT
ENV YARN_VERSION=1.22.22
# Thu, 04 Dec 2025 21:48:52 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 04 Dec 2025 21:48:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 21:48:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 21:48:52 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ce0aeb3ab5d5bfbad582e8066deaad106a2f9283749fcafb0511016ae31563`  
		Last Modified: Thu, 04 Dec 2025 21:49:25 GMT  
		Size: 53.1 MB (53137069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f14b2ebcaa98fd13e079c1dc43abe38249c3a39d7ac393147edd7ee762c0ebb`  
		Last Modified: Thu, 04 Dec 2025 21:49:20 GMT  
		Size: 1.3 MB (1262989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f35796f2d8660aaf8bfec62343eab003b5707cd6b01bff3952d16d407f058f`  
		Last Modified: Thu, 04 Dec 2025 21:49:20 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-alpine3.23` - unknown; unknown

```console
$ docker pull node@sha256:41f8ec22d4958722da7ce25d4bf3552ccaf65ef498195798e3ad90dbe41738e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.4 KB (398352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1000e1b73440822ccaee79ebbc7625e1f5092e7f82d1e64dc20760cd9f1be0f9`

```dockerfile
```

-	Layers:
	-	`sha256:7ed10c2dd5309c331b9b67c98d3691ee16fcd861d10da9b97f9cb0f06604e76f`  
		Last Modified: Thu, 04 Dec 2025 22:42:36 GMT  
		Size: 372.4 KB (372357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda4b73761352ff47392e26e2107d68aa49c1202d8a229a6d5492289f33c388f`  
		Last Modified: Thu, 04 Dec 2025 22:42:37 GMT  
		Size: 26.0 KB (25995 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-alpine3.23` - linux; s390x

```console
$ docker pull node@sha256:52f3a9d9d3f00872fe53017733ada552b4febaf36dc75d62d92976510ddd777a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58789265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a473b301adb7c3ebe7a227fee7220bcf0efb09bb826853b255c0236504d84e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 23:26:02 GMT
ENV NODE_VERSION=25.2.1
# Thu, 04 Dec 2025 23:26:02 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="2cacd704a60accb358852fd565ae85ef83bd368578037bf936b8597ce2935773" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 04 Dec 2025 23:26:02 GMT
ENV YARN_VERSION=1.22.22
# Thu, 04 Dec 2025 23:26:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 04 Dec 2025 23:26:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 23:26:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 23:26:11 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8519eb4398857a15e61c7f3341274a413cff527cc1d440c3e89630dd5be1fa1f`  
		Last Modified: Thu, 04 Dec 2025 23:26:52 GMT  
		Size: 53.8 MB (53802035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94233143e3e3789cd564822a5295247b48eec9436cc3afe07b0ca3ee7f571da8`  
		Last Modified: Thu, 04 Dec 2025 23:26:48 GMT  
		Size: 1.3 MB (1262974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46c5449db31080462efcf0a4959f651262a22b58407e27e5cb33523159fdbdc`  
		Last Modified: Thu, 04 Dec 2025 23:26:48 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-alpine3.23` - unknown; unknown

```console
$ docker pull node@sha256:b008a620024b47c34607f6b90ea5c771181d4f5c6bb256dcd0d973028963b4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.0 KB (398031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c248fbbb055539541b60f24603d01a431edfae212023ea26867bc959c358367e`

```dockerfile
```

-	Layers:
	-	`sha256:5b40d8e648eab54b9cb73005f3f31fc19b5ed672015f500a51453cd0b40bcf16`  
		Last Modified: Fri, 05 Dec 2025 01:40:15 GMT  
		Size: 372.2 KB (372228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:886b66869fcf9d5fb820fff0f6d9bab1dca6187c5c60f30b7fe40ad88a47ec4b`  
		Last Modified: Fri, 05 Dec 2025 01:40:16 GMT  
		Size: 25.8 KB (25803 bytes)  
		MIME: application/vnd.in-toto+json

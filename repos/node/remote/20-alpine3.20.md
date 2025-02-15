## `node:20-alpine3.20`

```console
$ docker pull node@sha256:3488b10bf958af7125a176419d2d8a9937d895bf124012aae811651988d2ffe6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `node:20-alpine3.20` - linux; amd64

```console
$ docker pull node@sha256:d4b8042fdb02ab03737ac36b5ebf7f316a595a8350829ef79339ff5f0b33aaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47726589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee121a5b860504a045d281dbd0e65b60ac58418d9a19c5728a1d85be5e5a5ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 10 Feb 2025 15:34:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
ENV NODE_VERSION=20.18.3
# Mon, 10 Feb 2025 15:34:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="e559c7e9fbaca994cdf25f116257bd5e48851f82eeddbc1a56857a1f9a58d882" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENV YARN_VERSION=1.22.22
# Mon, 10 Feb 2025 15:34:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc93b75590f603214a47b554300b1440e6d7230f29d4c91c464704ddb7f33ff1`  
		Last Modified: Fri, 14 Feb 2025 22:40:42 GMT  
		Size: 42.7 MB (42711812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7f2bda001d3fd9c3197c56448ba6f54872c939349ca2c9a7c6dc309c273c17`  
		Last Modified: Fri, 14 Feb 2025 22:40:41 GMT  
		Size: 1.4 MB (1387434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fdad86d21ac4e1e14b4668a8bd57ab3476b34986dc7d2a767452194bc9b27e`  
		Last Modified: Fri, 14 Feb 2025 22:40:41 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-alpine3.20` - unknown; unknown

```console
$ docker pull node@sha256:9cd16e73fbd6592d6527c26d2608c18276720ed07ac5993f06d02da0cc5ec4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.1 KB (389122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a53552737b472108f92fec8ca170d8559fef8653c9fefec6a1372f916c9c96a`

```dockerfile
```

-	Layers:
	-	`sha256:43d620a2a8b6c4134c3eac3b656bbe2b2aec7daceee95c107789787c3964f6f4`  
		Last Modified: Fri, 14 Feb 2025 22:39:03 GMT  
		Size: 365.6 KB (365620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20af8c7100dfa30a7b5a0e67b7fdbf12ee3ed748db2d4d92a1460ca9c62398a0`  
		Last Modified: Fri, 14 Feb 2025 22:39:03 GMT  
		Size: 23.5 KB (23502 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-alpine3.20` - linux; arm variant v6

```console
$ docker pull node@sha256:6abe81caf6d2efcf35528dc81489a9495bcd73433e6c218f67f1d46f4ecab3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45766442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2affec970a7170d0063f04549b27bfecfa4d7a9e8190a422d498f677f85e4c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 10 Feb 2025 15:34:31 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
ENV NODE_VERSION=20.18.3
# Mon, 10 Feb 2025 15:34:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="e559c7e9fbaca994cdf25f116257bd5e48851f82eeddbc1a56857a1f9a58d882" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENV YARN_VERSION=1.22.22
# Mon, 10 Feb 2025 15:34:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 19:26:24 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f728e64ebb9f6fc95afcdc30342d1120ee9a3f0d02f30f8fe5438ce0251d049e`  
		Last Modified: Sat, 15 Feb 2025 07:39:33 GMT  
		Size: 41.0 MB (41006033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e276e2b25313303de66f3343252ad7ba9eca266f518bd9fba1b6678b83f9fe6b`  
		Last Modified: Sat, 15 Feb 2025 07:39:31 GMT  
		Size: 1.4 MB (1387432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324daa4723c25c806228708fee877006ec2f94895042074162369535eb8efeb1`  
		Last Modified: Sat, 15 Feb 2025 06:08:38 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-alpine3.20` - unknown; unknown

```console
$ docker pull node@sha256:ea7c7cc7fd9a4e4c3fd2ca81dd13daaef29965be0576c0a127ce18ce5ecc3bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 KB (23376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a44ce586a4b441053d411a4d15d534560ff406e4233277c2cb1d1deac2b8fc`

```dockerfile
```

-	Layers:
	-	`sha256:681cd20463741faacfe303969144a21986e5277a1cc599f9f8eb79f013a1d552`  
		Last Modified: Sat, 15 Feb 2025 07:39:17 GMT  
		Size: 23.4 KB (23376 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-alpine3.20` - linux; arm variant v7

```console
$ docker pull node@sha256:011a302304af84c1b11a29abb80e3dafe400a52390b43ed6d4f8a53e87affc5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44929639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87edfb384b470b16eabae7e100adbad44e0f9c5a82054fbefc2f53bd9eded96f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 10 Feb 2025 15:34:31 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
ENV NODE_VERSION=20.18.3
# Mon, 10 Feb 2025 15:34:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="e559c7e9fbaca994cdf25f116257bd5e48851f82eeddbc1a56857a1f9a58d882" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENV YARN_VERSION=1.22.22
# Mon, 10 Feb 2025 15:34:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 14:35:10 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fa832e16604ef458c03f8fdd35c823d71bfa5679f3726645f7aaaafd35148e`  
		Last Modified: Sat, 15 Feb 2025 05:23:45 GMT  
		Size: 40.4 MB (40445786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f514eb33568d0c4b994030a43bebff1a0b5140a7fbdd36723cabb12bc9f0c1c`  
		Last Modified: Sat, 15 Feb 2025 05:23:44 GMT  
		Size: 1.4 MB (1387439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b9b66c79f060c2fb1347c7451f13d36b1808fb6e0768f0e70be9dd71fc4f92`  
		Last Modified: Sat, 15 Feb 2025 05:23:43 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-alpine3.20` - unknown; unknown

```console
$ docker pull node@sha256:e555803b26472c0ea4d5dc41f1ba9f998dc780172e7b24790baa5d1a22a0632c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 KB (389247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6730f2d8bd925d12ed2b79501d3a2b9dba7ff6b94cc51bc34a11306b0e658f20`

```dockerfile
```

-	Layers:
	-	`sha256:30f94fea87af8a3483f2b8229fd0b59e1736f06d8ffe15ee1d55f706d6f8a92a`  
		Last Modified: Sat, 15 Feb 2025 07:39:18 GMT  
		Size: 365.7 KB (365656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a04b4e18c03fe8fb3752d198c1596a79bdaa1740b2cd8e0a21c18e021d4bd5c2`  
		Last Modified: Sat, 15 Feb 2025 07:39:18 GMT  
		Size: 23.6 KB (23591 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull node@sha256:054fa939d6f241eb5fe7082987948cf28bed2f8dc3ad862cc09e20e57bf94e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47714406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677fad623d56646054041fef897a187085d19cbadfade06741a29912bb8d944a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 10 Feb 2025 15:34:31 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
ENV NODE_VERSION=20.18.3
# Mon, 10 Feb 2025 15:34:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="e559c7e9fbaca994cdf25f116257bd5e48851f82eeddbc1a56857a1f9a58d882" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENV YARN_VERSION=1.22.22
# Mon, 10 Feb 2025 15:34:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90728d82946d5b2ef8a742b77aa771ece70c448ea20e647074f373af879b129`  
		Last Modified: Sat, 15 Feb 2025 04:42:36 GMT  
		Size: 42.2 MB (42235362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9297aeac5624afb92875c4e3afccaaa0d6ed298f65c0a27f41480d228d94cd`  
		Last Modified: Sat, 15 Feb 2025 04:42:35 GMT  
		Size: 1.4 MB (1387434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1415d8ec5d9d9e04624e8e95bc393f86f24562a26a39baea5d0917c7c7d416f`  
		Last Modified: Sat, 15 Feb 2025 03:45:47 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-alpine3.20` - unknown; unknown

```console
$ docker pull node@sha256:355815cecb755fdc68b3352dfe66a4ec14ab3a014ac028af228bac9f511cc341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.3 KB (389296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af83ad210bf44305fc3588ea5c5d9c0e89a0fcf0cc22905d8653a19b9f4634e`

```dockerfile
```

-	Layers:
	-	`sha256:3515fd1a243961eac3a8cecbee8b206e8f2e6c74f398c51419adf022846e5986`  
		Last Modified: Sat, 15 Feb 2025 04:38:51 GMT  
		Size: 365.7 KB (365676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1409cba83a7de0bc18cbafe544f80f7d63cccb30afcde2b4e7827a4d23716d1d`  
		Last Modified: Sat, 15 Feb 2025 04:38:51 GMT  
		Size: 23.6 KB (23620 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-alpine3.20` - linux; ppc64le

```console
$ docker pull node@sha256:14472529524472eb28f69b14480c14cfdd3388c7f61d01ca13aba0aebe85b672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24f41b846c3f9e122d63fa1335d26f0d2a6ca8fcee7eb60518d14ba193f92fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 10 Feb 2025 15:34:31 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
ENV NODE_VERSION=20.18.3
# Mon, 10 Feb 2025 15:34:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="e559c7e9fbaca994cdf25f116257bd5e48851f82eeddbc1a56857a1f9a58d882" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENV YARN_VERSION=1.22.22
# Mon, 10 Feb 2025 15:34:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 14:35:49 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcb92942ac0e6a548db2ff8f20318c5030af3b41e67251ecd49a0cfc1dda09c`  
		Last Modified: Fri, 14 Feb 2025 22:49:25 GMT  
		Size: 45.3 MB (45309068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8e0176fd657f49348859bce39430c2e00acaf79bf537f040182df93fbaa5d3`  
		Last Modified: Fri, 14 Feb 2025 22:49:23 GMT  
		Size: 1.4 MB (1387443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b6fe26b13076f5bb3113b14db95d4b64ebbac457647ff28c868e06d734a8aa`  
		Last Modified: Fri, 14 Feb 2025 22:49:23 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-alpine3.20` - unknown; unknown

```console
$ docker pull node@sha256:da98e21de77d5f2bb5263ccdea2890f1fdd760e28448d692e899057b78c5347b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.3 KB (387251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8387798f8877360ec3bebbc3bd4270292e4254fffc099270be98e4ff5ab88b7`

```dockerfile
```

-	Layers:
	-	`sha256:2a360d0651c008e99a8704f87beff41bd76c272f9d844863393a9cd581d08130`  
		Last Modified: Fri, 14 Feb 2025 22:39:08 GMT  
		Size: 363.7 KB (363703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3ad621727a7fca8b43ab72db40a1406123f59135c2e8db0403873bd17b53f6`  
		Last Modified: Fri, 14 Feb 2025 22:39:08 GMT  
		Size: 23.5 KB (23548 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-alpine3.20` - linux; s390x

```console
$ docker pull node@sha256:0c18ad85e5dbac4a2a72168d0bb69547f37252e17cfa2742d960a97d4c5b2984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48534762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682bb880e42587785920c53ce61a3c8b18cc9e2b0c7610e6eae8cee8f12e301d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 10 Feb 2025 15:34:31 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
ENV NODE_VERSION=20.18.3
# Mon, 10 Feb 2025 15:34:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="e559c7e9fbaca994cdf25f116257bd5e48851f82eeddbc1a56857a1f9a58d882" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENV YARN_VERSION=1.22.22
# Mon, 10 Feb 2025 15:34:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 14:36:22 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1ceb9ead24ec1fdc3b6fa4f6c0835ec7276428e9f97a1f5b0e8e94a76310b6`  
		Last Modified: Sat, 15 Feb 2025 05:27:32 GMT  
		Size: 43.7 MB (43682754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ead8cc3545d852dcc7bcbdd2d1030c6aad8c8044ec01e3f2a57f65931c9416`  
		Last Modified: Sat, 15 Feb 2025 05:27:29 GMT  
		Size: 1.4 MB (1387443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d22e19ef7fb451c560761379288cc268be70a7f81d32cd6a0427bde58e42cc`  
		Last Modified: Sat, 15 Feb 2025 05:27:28 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-alpine3.20` - unknown; unknown

```console
$ docker pull node@sha256:56df5862b6f0492a95a5ba9749ea161b4c5e9003cc3fdddc040472324bbe6bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.2 KB (387170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b08a377b4354dc41d86b4cd8bc96da3b0085ca3327b68ea511f7328c3bf2100`

```dockerfile
```

-	Layers:
	-	`sha256:29e52cd4217a9eb3bdede66bea271888060060787fa7a86790e949c39c0c5fa6`  
		Last Modified: Sat, 15 Feb 2025 04:38:53 GMT  
		Size: 363.7 KB (363669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e5f8a67e3f3d6322ae3b7f4cbe64230a39205f20be0223b24a61c6712063d0`  
		Last Modified: Sat, 15 Feb 2025 04:38:53 GMT  
		Size: 23.5 KB (23501 bytes)  
		MIME: application/vnd.in-toto+json

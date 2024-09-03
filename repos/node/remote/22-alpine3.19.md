## `node:22-alpine3.19`

```console
$ docker pull node@sha256:a17f4849b1397ac8c084a2b986c4f45ade785949f734e787c1db6b23f49c8b49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `node:22-alpine3.19` - linux; amd64

```console
$ docker pull node@sha256:e44d791512a92085db7b8f538b4a64f36f403fcf86ef7cd63c4e08553d120cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53583655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c16c7560290a57ce762afa97173474e1200f6c2d927d8f8624664bced6c10b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 15:33:51 GMT
ENV NODE_VERSION=22.8.0
# Tue, 03 Sep 2024 15:33:51 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="03684363352ac907758b53f3bc094bcf128fa8570de9a4657531c1c54f9a335c" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 03 Sep 2024 15:33:51 GMT
ENV YARN_VERSION=1.22.22
# Tue, 03 Sep 2024 15:33:51 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 03 Sep 2024 15:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 15:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 15:33:51 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ea1a473e5eb7458a514e52e031b653c87d6476f805713432652cf2103ac646`  
		Last Modified: Tue, 03 Sep 2024 19:58:36 GMT  
		Size: 48.8 MB (48776947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00f3f69521524c32eb3f3c4e4c5c6bce2f7ae0efad3433236723cc4b4d6b8cd`  
		Last Modified: Tue, 03 Sep 2024 19:58:35 GMT  
		Size: 1.4 MB (1387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0673476fe186d9100b884040097dfb607cb9d270328f36a87a1521dba2a203`  
		Last Modified: Tue, 03 Sep 2024 19:58:35 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:22-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:92d4176cd7cdf10d7d1928c1d565ec1d7203d2229143a6ce9cc4b51136555e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.4 KB (373384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a677f970cb1772cb76fda7ff6cb4b43b4897b8aea9a37b9e8d9cbd127900720e`

```dockerfile
```

-	Layers:
	-	`sha256:c5a3bb7c26ad6ff5c97c70b4546b391ae6032044294a3fb74e8a219719f4a24f`  
		Last Modified: Tue, 03 Sep 2024 19:58:35 GMT  
		Size: 349.2 KB (349197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f7d4f6c019d8fe73cf2218bfec8e2c64ef6c9321b80e3aeb8eeb8e284eca54`  
		Last Modified: Tue, 03 Sep 2024 19:58:35 GMT  
		Size: 24.2 KB (24187 bytes)  
		MIME: application/vnd.in-toto+json

### `node:22-alpine3.19` - linux; arm variant v6

```console
$ docker pull node@sha256:0bb68819e3a40af524ca9a216b2fca3b44f627f35a8f8dcfef9bdf5c8fdec1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51497158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571c729ad1d8cf9ca91fcd6190b99c6d9e2f708095d989233a3a29feb0caeb9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 16:24:07 GMT
ENV NODE_VERSION=22.7.0
# Thu, 22 Aug 2024 16:24:07 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="164a9b11ce4ea8cfe87e0db9f29f4becb6fbb59c2ed4f76a64eb1d0e877c3ed4" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 22 Aug 2024 16:24:07 GMT
ENV YARN_VERSION=1.22.22
# Thu, 22 Aug 2024 16:24:07 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 22 Aug 2024 16:24:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Aug 2024 16:24:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Aug 2024 16:24:07 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ea76ba9377812e4784955cc06ab44f01263d84649093507253cf26f7af5462`  
		Last Modified: Thu, 22 Aug 2024 21:26:32 GMT  
		Size: 46.9 MB (46933817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4109f01e2c79a7c5dbc8c9b0d34ad8354789a6ac43b4e8d94db321e70b76559e`  
		Last Modified: Thu, 22 Aug 2024 21:26:31 GMT  
		Size: 1.4 MB (1387221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e3d3c4da33335414f85da11e1663d6f67ef3de3aaad91e44c0ed8423a4e810`  
		Last Modified: Thu, 22 Aug 2024 21:26:30 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:22-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:252dd92d9d53b11a090d5744a627546d05b3c5851ca70308f0c5e6d41781a467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 KB (24059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdd282c4ec2f493db90bd8eb3da929a89703feb315e05ab23f62bbb1692ce8a`

```dockerfile
```

-	Layers:
	-	`sha256:cb9306f88351a5b89279672a12e18c712177eafb802f1cdb5fc179ad176f5233`  
		Last Modified: Thu, 22 Aug 2024 21:26:30 GMT  
		Size: 24.1 KB (24059 bytes)  
		MIME: application/vnd.in-toto+json

### `node:22-alpine3.19` - linux; arm variant v7

```console
$ docker pull node@sha256:e3cb61af3c0af2d018f5573cc24250afaccc8810b59c38be538ca62e974e5cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50576698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba741f72ed7bca3a0c5450591e4f2d08861563feebe130fcf928cd650e0eee61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 16:24:07 GMT
ENV NODE_VERSION=22.7.0
# Thu, 22 Aug 2024 16:24:07 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="164a9b11ce4ea8cfe87e0db9f29f4becb6fbb59c2ed4f76a64eb1d0e877c3ed4" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 22 Aug 2024 16:24:07 GMT
ENV YARN_VERSION=1.22.22
# Thu, 22 Aug 2024 16:24:07 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 22 Aug 2024 16:24:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Aug 2024 16:24:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Aug 2024 16:24:07 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3bdad0aa63bd3377120048d72ccdf4c7459d3d515d13a29445145fa30a8ca9`  
		Last Modified: Thu, 22 Aug 2024 21:26:24 GMT  
		Size: 46.3 MB (46261936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedbdcd898463068b7419846272b2760f32cc8f9c90c4863a0ac2d1ce9eb2e96`  
		Last Modified: Thu, 22 Aug 2024 21:26:23 GMT  
		Size: 1.4 MB (1387212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012403b3960fe49dcb0e5ca29d725392a79b6c20394514da2a595b0c93becfba`  
		Last Modified: Thu, 22 Aug 2024 21:26:22 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:22-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:7c62a2ecb9e26cd0df8b751a3251ca53500e0b5abb4711b617871f3b70d34435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.5 KB (373519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b6f1b76b8421fd041b2c05f327267e096236efb62e3dc267fc6e01af635d08`

```dockerfile
```

-	Layers:
	-	`sha256:772b92d4d051472a22e65601e52cbaad9ef95dc62e48a5ba15b4a0d86b35ac94`  
		Last Modified: Thu, 22 Aug 2024 21:26:22 GMT  
		Size: 349.2 KB (349241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72dd693851919d9a90af745068961705419e983f9b4fec871b7b4eadd40a7fbb`  
		Last Modified: Thu, 22 Aug 2024 21:26:22 GMT  
		Size: 24.3 KB (24278 bytes)  
		MIME: application/vnd.in-toto+json

### `node:22-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull node@sha256:06b4b50c385919f0228874cc12202f4e60c1ba415e3417e1c677eb1ac75b2465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52923227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cdbba8e71b2557274ad72a8f41c0f64af22508f53465412b0a481ced6c1db0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 16:24:07 GMT
ENV NODE_VERSION=22.7.0
# Thu, 22 Aug 2024 16:24:07 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="164a9b11ce4ea8cfe87e0db9f29f4becb6fbb59c2ed4f76a64eb1d0e877c3ed4" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 22 Aug 2024 16:24:07 GMT
ENV YARN_VERSION=1.22.22
# Thu, 22 Aug 2024 16:24:07 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 22 Aug 2024 16:24:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Aug 2024 16:24:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Aug 2024 16:24:07 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981980f29982e44b625818b53bb761f4345e5a8858fd7ac80d809771d661060c`  
		Last Modified: Thu, 22 Aug 2024 20:46:59 GMT  
		Size: 48.2 MB (48177108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76c9e5b25de36622708ab512742e2d460b295c4702cee26115e1bfcdedcffe1`  
		Last Modified: Thu, 22 Aug 2024 20:46:58 GMT  
		Size: 1.4 MB (1387216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c81bcac503e6a771683726f5d646dd6f1331d9a6130471a0d21675592ae36d`  
		Last Modified: Thu, 22 Aug 2024 20:46:57 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:22-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:bea3100a1cc7ff27ce125799ac7b204237174d6d85d1013152f28d66b39eb96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.8 KB (373764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570332284e1833fe7d05fcf102a30ac66f3442c73f82bbb3629b63280476bacc`

```dockerfile
```

-	Layers:
	-	`sha256:f97874059dc82817832f02ff615d69d966000781daf88d2b643ff1d10f860e4f`  
		Last Modified: Thu, 22 Aug 2024 20:46:58 GMT  
		Size: 349.3 KB (349265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca5944e8664595ff3534b4f20ebedc74c5d706922338bf9ad6632862ff9223b6`  
		Last Modified: Thu, 22 Aug 2024 20:46:57 GMT  
		Size: 24.5 KB (24499 bytes)  
		MIME: application/vnd.in-toto+json

### `node:22-alpine3.19` - linux; s390x

```console
$ docker pull node@sha256:7471d167bfc59becdbe1fa43ec7fbb7724a1b663ef0d8315eb0192fd62428720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54482107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25725e7293eb721f8de9bf484175257404ca4f5aee5dec0c17298d5ebd7379d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 16:24:07 GMT
ENV NODE_VERSION=22.7.0
# Thu, 22 Aug 2024 16:24:07 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="164a9b11ce4ea8cfe87e0db9f29f4becb6fbb59c2ed4f76a64eb1d0e877c3ed4" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 22 Aug 2024 16:24:07 GMT
ENV YARN_VERSION=1.22.22
# Thu, 22 Aug 2024 16:24:07 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 22 Aug 2024 16:24:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Aug 2024 16:24:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Aug 2024 16:24:07 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1892720a94c633b7141423e5410e71613dc236df233257d203e00c5b20cfc0`  
		Last Modified: Thu, 22 Aug 2024 20:54:21 GMT  
		Size: 49.8 MB (49841375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442f4ef19bda492547f41ab4d93baa3437a2295a7f4af6ab918506f3281c2278`  
		Last Modified: Thu, 22 Aug 2024 20:54:20 GMT  
		Size: 1.4 MB (1387209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616098480d96223e0e108655e92888e70fe355e0441c44fd23511677f3916d33`  
		Last Modified: Thu, 22 Aug 2024 20:54:20 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:22-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:aca37c625c425bcdd4a1c5c6e4c2f19b7571678556f34c3858ce00498d879c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.4 KB (371430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e724b8fc5f7851044bb896e39d40b65cc66bb9e353833bd73ccefd038c223cce`

```dockerfile
```

-	Layers:
	-	`sha256:54596885e61f0fc7e45937e300479594c56376d5cc2c991801e031ee37caf0cb`  
		Last Modified: Thu, 22 Aug 2024 20:54:20 GMT  
		Size: 347.2 KB (347243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af88be24f512f21df7aac477c7146979717eb1ffb20791caaa64e15021825a54`  
		Last Modified: Thu, 22 Aug 2024 20:54:20 GMT  
		Size: 24.2 KB (24187 bytes)  
		MIME: application/vnd.in-toto+json

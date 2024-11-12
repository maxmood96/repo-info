## `mongo-express:1-20-alpine3.19`

```console
$ docker pull mongo-express@sha256:0d2ec1b4f332c2b65c700f5bcfdef07ab9bb1b8d0f6c3403fb7f4ba6802e802c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1-20-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:0f4590ea2a86d5fefaf255fd94a4f41da2606cb5845e808c7414d32c3a318584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61852402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253ff06daba13236ac3ea8fd2ae1750a16309f85df3f344db17844568f6384b5`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.18.0
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="757bba0adff8eaadfa7f9be2c87a35d5010ac3f71b5527e57385218c806a4fa4" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["node"]
# Fri, 08 Mar 2024 19:22:05 GMT
RUN set -eux;     apk add --no-cache         bash         tini # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
WORKDIR /app
# Fri, 08 Mar 2024 19:22:05 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Fri, 08 Mar 2024 19:22:05 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Fri, 08 Mar 2024 19:22:05 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     yarn remove --all;     yarn workspaces focus --production;     yarn cache clean;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Fri, 08 Mar 2024 19:22:05 GMT
EXPOSE map[8081/tcp:{}]
# Fri, 08 Mar 2024 19:22:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb2de3cf913f80247689b3a7cee8d65214f5410e151f3f73d7ab565b83f7d85`  
		Last Modified: Tue, 12 Nov 2024 02:39:49 GMT  
		Size: 42.6 MB (42618763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c81de09019a8cca7d60be5fc398fa152cc91eb643b864a193ba145d65acb911`  
		Last Modified: Tue, 12 Nov 2024 02:39:49 GMT  
		Size: 1.4 MB (1387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963e91d8b9624d54e58061d5a71e7fe9ac30fd7d436914491c68e6b6c3f78022`  
		Last Modified: Tue, 12 Nov 2024 02:39:48 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa660385a9c87717ceabcdac27d7b4674dae0b4421f67861e440e9e083ecadfd`  
		Last Modified: Tue, 12 Nov 2024 03:14:32 GMT  
		Size: 784.6 KB (784641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d90e7e104f13326e561741475451dfbb35c23821593ef94d440978cf1dae9fc`  
		Last Modified: Tue, 12 Nov 2024 03:14:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e3ab92f90624832d627c218457314486ddbe36c7a8735b73c3430199589e5b`  
		Last Modified: Tue, 12 Nov 2024 03:14:32 GMT  
		Size: 13.6 MB (13640658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1972de9119ddb81fb3aed1148313ee4d6870e866ce2363ff40739f1ba54dcafe`  
		Last Modified: Tue, 12 Nov 2024 03:14:32 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-20-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:1e50ba0a53c7095da6462121ef96fb884dc6b5e987d927620d4a65de66c20a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c131d97d6dbbd532a1274a5d218ef6c6c7808342d2f8dcc06bd87111162da99`

```dockerfile
```

-	Layers:
	-	`sha256:f8e91d8714f48942b85bf5b615ea96845e8247d4a783d7dc9e47b20ee172fa4f`  
		Last Modified: Tue, 12 Nov 2024 03:14:32 GMT  
		Size: 997.0 KB (996978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7c99f57787bf2c68db34064810bd905e4fc80aba6a3e100f37ca09e5fc79ff7`  
		Last Modified: Tue, 12 Nov 2024 03:14:32 GMT  
		Size: 15.3 KB (15298 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1-20-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:3dbefa4f16a998e9b141a7bf70587d2a106b3f6a069c8bcb469eeea6a40a4e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61426582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c19fa78d3000d5a7abfaf77235687cfe6d54fd3bb0d4ef12c3eae7b20f949bf`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.18.0
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="757bba0adff8eaadfa7f9be2c87a35d5010ac3f71b5527e57385218c806a4fa4" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.22
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["node"]
# Fri, 08 Mar 2024 19:22:05 GMT
RUN set -eux;     apk add --no-cache         bash         tini # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
WORKDIR /app
# Fri, 08 Mar 2024 19:22:05 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Fri, 08 Mar 2024 19:22:05 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Fri, 08 Mar 2024 19:22:05 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     yarn remove --all;     yarn workspaces focus --production;     yarn cache clean;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Fri, 08 Mar 2024 19:22:05 GMT
EXPOSE map[8081/tcp:{}]
# Fri, 08 Mar 2024 19:22:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676d822d150c6a49ff3cce04f0940b2d543496810571bcd10e628c8efc9c896e`  
		Last Modified: Fri, 04 Oct 2024 19:21:16 GMT  
		Size: 42.2 MB (42176129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb46b17ee8146c9f50536db08f6addb58bf75ae9e43dbc4a70009d24e314e819`  
		Last Modified: Fri, 04 Oct 2024 19:21:15 GMT  
		Size: 1.4 MB (1387232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3faf4dc9cf87a5d2f8b398397ec4fd42bf201f039fa135c55c9f8eeb7f3482`  
		Last Modified: Fri, 04 Oct 2024 19:21:14 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708fabb713bec3dc521d4a61e23bdc5719d40fdc97ed7356b0dd8241dce528fe`  
		Last Modified: Fri, 04 Oct 2024 19:54:57 GMT  
		Size: 862.4 KB (862417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6823abdd115031c262c88b0f1f10a7ced588b5b719b125315a63a330dfaa70a0`  
		Last Modified: Fri, 04 Oct 2024 19:54:37 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54693a45fb50b5d2f2fed9cea2491416241c0bf5720c904f37ebb341f4709651`  
		Last Modified: Fri, 04 Oct 2024 19:54:57 GMT  
		Size: 13.6 MB (13640315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7417bfcf953a1ffe621ee632f17b05df973db02cd933a974ee403dc28f357e89`  
		Last Modified: Fri, 04 Oct 2024 19:54:57 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-20-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:a00e0f2222da5a293ebe97a17567ec2b9a8a5a869ccd5aa5abb3c1929857cf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.1 KB (946108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56b091dce0cf235f4c58b77d3b78571747c8fcc1645164824ab4a493b0e6845`

```dockerfile
```

-	Layers:
	-	`sha256:ae312582370aabcdc898dd99ac9ad33b64aa8b8fc7ee7218c5ad2fd0ecd1f6c1`  
		Last Modified: Fri, 04 Oct 2024 19:54:56 GMT  
		Size: 930.7 KB (930703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47eef6a48698ebb067ad46ce9bdb983b979deddfab63e898a6c6a518b011bdcb`  
		Last Modified: Fri, 04 Oct 2024 19:54:56 GMT  
		Size: 15.4 KB (15405 bytes)  
		MIME: application/vnd.in-toto+json

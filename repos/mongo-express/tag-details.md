<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mongo-express`

-	[`mongo-express:1`](#mongo-express1)
-	[`mongo-express:1-18`](#mongo-express1-18)
-	[`mongo-express:1-18-alpine3.18`](#mongo-express1-18-alpine318)
-	[`mongo-express:1-18-alpine3.19`](#mongo-express1-18-alpine319)
-	[`mongo-express:1-20`](#mongo-express1-20)
-	[`mongo-express:1-20-alpine3.18`](#mongo-express1-20-alpine318)
-	[`mongo-express:1-20-alpine3.19`](#mongo-express1-20-alpine319)
-	[`mongo-express:1.0`](#mongo-express10)
-	[`mongo-express:1.0-18`](#mongo-express10-18)
-	[`mongo-express:1.0-18-alpine3.18`](#mongo-express10-18-alpine318)
-	[`mongo-express:1.0-18-alpine3.19`](#mongo-express10-18-alpine319)
-	[`mongo-express:1.0-20`](#mongo-express10-20)
-	[`mongo-express:1.0-20-alpine3.18`](#mongo-express10-20-alpine318)
-	[`mongo-express:1.0-20-alpine3.19`](#mongo-express10-20-alpine319)
-	[`mongo-express:1.0.2`](#mongo-express102)
-	[`mongo-express:1.0.2-18`](#mongo-express102-18)
-	[`mongo-express:1.0.2-18-alpine3.18`](#mongo-express102-18-alpine318)
-	[`mongo-express:1.0.2-18-alpine3.19`](#mongo-express102-18-alpine319)
-	[`mongo-express:1.0.2-20`](#mongo-express102-20)
-	[`mongo-express:1.0.2-20-alpine3.18`](#mongo-express102-20-alpine318)
-	[`mongo-express:1.0.2-20-alpine3.19`](#mongo-express102-20-alpine319)
-	[`mongo-express:latest`](#mongo-expresslatest)

## `mongo-express:1`

```console
$ docker pull mongo-express@sha256:98ad29b0d7cbeeba8f4640cdcd11e097081ed0ca27c89b4ee0cde63e3bfe53f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1` - linux; amd64

```console
$ docker pull mongo-express@sha256:0cba5f35c950762b9093da01ae48c19e3088093eeef8cb119529fb298685552d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79724504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d527c213d73e59c6dcc7e8b090002a1f81503a790d78d47b34df8586ce8c252f`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 01:26:35 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 01:26:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 01:26:44 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 01:26:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 01:26:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 01:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 01:26:48 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:16:13 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:16:13 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:16:52 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:37 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:37 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:37 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:37 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:37 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7465dc4da3894941da9beb13e53fea672b4167e0031a049feea4cd6ed2cd79`  
		Last Modified: Sat, 02 Dec 2023 01:34:45 GMT  
		Size: 40.1 MB (40112458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7b2bf3cf64fb3d50ff099853b0df6438ea6163f4d9d2a7880856bd36a59ba2`  
		Last Modified: Sat, 02 Dec 2023 01:34:40 GMT  
		Size: 2.3 MB (2342890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3604fe7c8f3c53b8058f060dce2cfe269aad37881cabc3fa7b88c926470e9488`  
		Last Modified: Sat, 02 Dec 2023 01:34:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef732f87d67b9f901f90ed568ca4b4cea78c7d2a37219f3a6e76d7cc2d7a75cd`  
		Last Modified: Sat, 06 Jan 2024 01:18:28 GMT  
		Size: 802.3 KB (802311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2ade8248554eb9e4592da34eccdc1e3b1097a8d22046f414f26b3ebf05d2b0`  
		Last Modified: Sat, 06 Jan 2024 01:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bb6e5f1580826a520151543dc3f7e3e536b326b7aa1e21ef81ce4480e08f4c`  
		Last Modified: Sat, 06 Jan 2024 01:18:36 GMT  
		Size: 33.1 MB (33062997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b209d7438a256fbd0fdaf2e7fb7d233773023b8019b2928737937d51026977`  
		Last Modified: Tue, 16 Jan 2024 18:34:34 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:a6846e70e124e9567bf389cf03d48b675f936ced5e4c0b65870cbe7062318a3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79444186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b30b6db7b34865b6126fd73f277de5fb3c193570fd3243921d7da8d63554c9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 03:48:51 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 04:09:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 04:09:30 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 04:09:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 04:09:35 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 04:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 04:09:35 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:56:27 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:56:27 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:56:59 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:50 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:50 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:50 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:50 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:50 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9cba98305bbc9b5b1acc82808c97ec2f1bdd0918782e26a4f249c89e8f5f1c`  
		Last Modified: Sat, 02 Dec 2023 04:17:12 GMT  
		Size: 39.8 MB (39817628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb1cdcfb3b6e7d1dbbdde57709e15e2c4bbdcac8f7c3da88459d74bc402c637`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 2.3 MB (2342686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266cff88a90930625e27a71f05f05b0bb69c1c3612e447e70131636367599c6c`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b233574749281abc1a8ad5a8fb4f54bd3aa2b79c58bd876195c947c20d3083fa`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 887.0 KB (886996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1254cb9a9f437dc36f890b22f67330bfbc4c76a86d4e1c845d093039c3455c1e`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca088f0889c67078200ebc911786a79a006f465a4c1e1a6fe630152a483e40bb`  
		Last Modified: Sat, 06 Jan 2024 01:58:29 GMT  
		Size: 33.1 MB (33062417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38362c10b0ee09dc1483616bb584925ef66302ceff20e0096c75f82025ca5fe`  
		Last Modified: Tue, 16 Jan 2024 18:40:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1-18`

```console
$ docker pull mongo-express@sha256:98ad29b0d7cbeeba8f4640cdcd11e097081ed0ca27c89b4ee0cde63e3bfe53f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1-18` - linux; amd64

```console
$ docker pull mongo-express@sha256:0cba5f35c950762b9093da01ae48c19e3088093eeef8cb119529fb298685552d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79724504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d527c213d73e59c6dcc7e8b090002a1f81503a790d78d47b34df8586ce8c252f`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 01:26:35 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 01:26:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 01:26:44 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 01:26:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 01:26:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 01:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 01:26:48 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:16:13 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:16:13 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:16:52 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:37 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:37 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:37 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:37 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:37 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7465dc4da3894941da9beb13e53fea672b4167e0031a049feea4cd6ed2cd79`  
		Last Modified: Sat, 02 Dec 2023 01:34:45 GMT  
		Size: 40.1 MB (40112458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7b2bf3cf64fb3d50ff099853b0df6438ea6163f4d9d2a7880856bd36a59ba2`  
		Last Modified: Sat, 02 Dec 2023 01:34:40 GMT  
		Size: 2.3 MB (2342890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3604fe7c8f3c53b8058f060dce2cfe269aad37881cabc3fa7b88c926470e9488`  
		Last Modified: Sat, 02 Dec 2023 01:34:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef732f87d67b9f901f90ed568ca4b4cea78c7d2a37219f3a6e76d7cc2d7a75cd`  
		Last Modified: Sat, 06 Jan 2024 01:18:28 GMT  
		Size: 802.3 KB (802311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2ade8248554eb9e4592da34eccdc1e3b1097a8d22046f414f26b3ebf05d2b0`  
		Last Modified: Sat, 06 Jan 2024 01:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bb6e5f1580826a520151543dc3f7e3e536b326b7aa1e21ef81ce4480e08f4c`  
		Last Modified: Sat, 06 Jan 2024 01:18:36 GMT  
		Size: 33.1 MB (33062997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b209d7438a256fbd0fdaf2e7fb7d233773023b8019b2928737937d51026977`  
		Last Modified: Tue, 16 Jan 2024 18:34:34 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1-18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:a6846e70e124e9567bf389cf03d48b675f936ced5e4c0b65870cbe7062318a3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79444186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b30b6db7b34865b6126fd73f277de5fb3c193570fd3243921d7da8d63554c9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 03:48:51 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 04:09:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 04:09:30 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 04:09:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 04:09:35 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 04:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 04:09:35 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:56:27 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:56:27 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:56:59 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:50 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:50 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:50 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:50 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:50 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9cba98305bbc9b5b1acc82808c97ec2f1bdd0918782e26a4f249c89e8f5f1c`  
		Last Modified: Sat, 02 Dec 2023 04:17:12 GMT  
		Size: 39.8 MB (39817628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb1cdcfb3b6e7d1dbbdde57709e15e2c4bbdcac8f7c3da88459d74bc402c637`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 2.3 MB (2342686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266cff88a90930625e27a71f05f05b0bb69c1c3612e447e70131636367599c6c`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b233574749281abc1a8ad5a8fb4f54bd3aa2b79c58bd876195c947c20d3083fa`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 887.0 KB (886996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1254cb9a9f437dc36f890b22f67330bfbc4c76a86d4e1c845d093039c3455c1e`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca088f0889c67078200ebc911786a79a006f465a4c1e1a6fe630152a483e40bb`  
		Last Modified: Sat, 06 Jan 2024 01:58:29 GMT  
		Size: 33.1 MB (33062417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38362c10b0ee09dc1483616bb584925ef66302ceff20e0096c75f82025ca5fe`  
		Last Modified: Tue, 16 Jan 2024 18:40:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1-18-alpine3.18`

```console
$ docker pull mongo-express@sha256:98ad29b0d7cbeeba8f4640cdcd11e097081ed0ca27c89b4ee0cde63e3bfe53f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1-18-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:0cba5f35c950762b9093da01ae48c19e3088093eeef8cb119529fb298685552d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79724504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d527c213d73e59c6dcc7e8b090002a1f81503a790d78d47b34df8586ce8c252f`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 01:26:35 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 01:26:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 01:26:44 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 01:26:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 01:26:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 01:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 01:26:48 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:16:13 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:16:13 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:16:52 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:37 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:37 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:37 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:37 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:37 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7465dc4da3894941da9beb13e53fea672b4167e0031a049feea4cd6ed2cd79`  
		Last Modified: Sat, 02 Dec 2023 01:34:45 GMT  
		Size: 40.1 MB (40112458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7b2bf3cf64fb3d50ff099853b0df6438ea6163f4d9d2a7880856bd36a59ba2`  
		Last Modified: Sat, 02 Dec 2023 01:34:40 GMT  
		Size: 2.3 MB (2342890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3604fe7c8f3c53b8058f060dce2cfe269aad37881cabc3fa7b88c926470e9488`  
		Last Modified: Sat, 02 Dec 2023 01:34:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef732f87d67b9f901f90ed568ca4b4cea78c7d2a37219f3a6e76d7cc2d7a75cd`  
		Last Modified: Sat, 06 Jan 2024 01:18:28 GMT  
		Size: 802.3 KB (802311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2ade8248554eb9e4592da34eccdc1e3b1097a8d22046f414f26b3ebf05d2b0`  
		Last Modified: Sat, 06 Jan 2024 01:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bb6e5f1580826a520151543dc3f7e3e536b326b7aa1e21ef81ce4480e08f4c`  
		Last Modified: Sat, 06 Jan 2024 01:18:36 GMT  
		Size: 33.1 MB (33062997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b209d7438a256fbd0fdaf2e7fb7d233773023b8019b2928737937d51026977`  
		Last Modified: Tue, 16 Jan 2024 18:34:34 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1-18-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:a6846e70e124e9567bf389cf03d48b675f936ced5e4c0b65870cbe7062318a3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79444186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b30b6db7b34865b6126fd73f277de5fb3c193570fd3243921d7da8d63554c9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 03:48:51 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 04:09:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 04:09:30 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 04:09:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 04:09:35 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 04:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 04:09:35 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:56:27 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:56:27 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:56:59 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:50 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:50 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:50 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:50 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:50 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9cba98305bbc9b5b1acc82808c97ec2f1bdd0918782e26a4f249c89e8f5f1c`  
		Last Modified: Sat, 02 Dec 2023 04:17:12 GMT  
		Size: 39.8 MB (39817628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb1cdcfb3b6e7d1dbbdde57709e15e2c4bbdcac8f7c3da88459d74bc402c637`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 2.3 MB (2342686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266cff88a90930625e27a71f05f05b0bb69c1c3612e447e70131636367599c6c`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b233574749281abc1a8ad5a8fb4f54bd3aa2b79c58bd876195c947c20d3083fa`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 887.0 KB (886996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1254cb9a9f437dc36f890b22f67330bfbc4c76a86d4e1c845d093039c3455c1e`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca088f0889c67078200ebc911786a79a006f465a4c1e1a6fe630152a483e40bb`  
		Last Modified: Sat, 06 Jan 2024 01:58:29 GMT  
		Size: 33.1 MB (33062417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38362c10b0ee09dc1483616bb584925ef66302ceff20e0096c75f82025ca5fe`  
		Last Modified: Tue, 16 Jan 2024 18:40:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1-18-alpine3.19`

```console
$ docker pull mongo-express@sha256:78bdf802ed37afc5a00c0689938a05c07eb0c044f5b78943cd01810892bc7165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1-18-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:76b2b013b8a9645dbe3ba2c1ce248ed227e1cd4f08a733f45f296565b8a9f8cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79837273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4579ff05115b2d8f428c5c77751ac90df4365faa4ad99f6686d11990a1f8f6f8`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Mon, 11 Dec 2023 18:37:13 GMT
ENV NODE_VERSION=18.19.0
# Mon, 11 Dec 2023 18:37:21 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Mon, 11 Dec 2023 18:37:22 GMT
ENV YARN_VERSION=1.22.19
# Mon, 11 Dec 2023 18:37:26 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 11 Dec 2023 18:37:26 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 11 Dec 2023 18:37:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Dec 2023 18:37:26 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:15:24 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:15:25 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:15:25 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:15:25 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:16:03 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:33 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:33 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:34 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:34 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:34 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f158788f409a5decd9495205daf4aa17df26d8219d6dc12acab5949342866fe`  
		Last Modified: Mon, 11 Dec 2023 18:40:25 GMT  
		Size: 40.2 MB (40236806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f028dff98271801e449c3ebac94a319851128c0ec687e13e00a68b2d98ec4700`  
		Last Modified: Mon, 11 Dec 2023 18:40:20 GMT  
		Size: 2.3 MB (2342755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f25c33705ddc3351cc4893fdc0a38405bdd0741643798918fa2b0146fd5a9d`  
		Last Modified: Mon, 11 Dec 2023 18:40:20 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fda4c5ad911063ff2d7ecb2537ab17e4c64d8b807138529677046ad06658793`  
		Last Modified: Sat, 06 Jan 2024 01:18:07 GMT  
		Size: 784.7 KB (784696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305d1a20d5027c21e855e059ee3b955582ec8dfe68e68216840344bbb4044e8f`  
		Last Modified: Sat, 06 Jan 2024 01:18:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d135d844ee3fac33c4b754dd160f532b303ec6d2dc049881149fb27b560663c`  
		Last Modified: Sat, 06 Jan 2024 01:18:15 GMT  
		Size: 33.1 MB (33063111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a1ca949f7cf2b0d7454dfddf692b268ba94311f570c0e5020a9ccda85718bf`  
		Last Modified: Tue, 16 Jan 2024 18:34:24 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1-18-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:b2d2b5a4d1d9b6ab5237ff3bdbbc30682d7c3f4c0569465d994e9f9221e02444
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79595014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76484dd7c6136aa629ff8682f1a65e3203c853cb75d602cbeea8c37f4417c31f`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Mon, 11 Dec 2023 18:40:05 GMT
ENV NODE_VERSION=18.19.0
# Mon, 11 Dec 2023 18:59:50 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Mon, 11 Dec 2023 18:59:50 GMT
ENV YARN_VERSION=1.22.19
# Mon, 11 Dec 2023 18:59:55 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 11 Dec 2023 18:59:55 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 11 Dec 2023 18:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Dec 2023 18:59:55 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:55:47 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:55:47 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:55:47 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:55:47 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:56:19 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:48 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:48 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:48 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:48 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:48 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7895eb72c1a145d166631d5a81c61bffd747783c52e8a1de9fa0e7d5871817`  
		Last Modified: Mon, 11 Dec 2023 19:02:51 GMT  
		Size: 40.0 MB (39978047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7049a133eb54d652049fa44657d24cef7298dc371ffab6e27f5cd5e53e62159f`  
		Last Modified: Mon, 11 Dec 2023 19:02:46 GMT  
		Size: 2.3 MB (2342730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90577567f13c6046278cbfa4a557cb5a19ed5f9c281ab540e84ddd8f74c71922`  
		Last Modified: Mon, 11 Dec 2023 19:02:45 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7fdab078a277850d97a71a23c41cbf45e5ac8092bc99a1429aa8247527f598`  
		Last Modified: Sat, 06 Jan 2024 01:58:06 GMT  
		Size: 862.4 KB (862441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1063d3ecd5c04feb20d959e43633106ee5d678f9e00be9c39fb4023bf1cffb35`  
		Last Modified: Sat, 06 Jan 2024 01:58:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dea9015fc2c949ef2ca11d0fffd8f60b647169e36e2e19d01045a8716ccec2`  
		Last Modified: Sat, 06 Jan 2024 01:58:12 GMT  
		Size: 33.1 MB (33062580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e762f944899eedd67688d768a6641886edc4c56739ac72560b5471ce8ad13c70`  
		Last Modified: Tue, 16 Jan 2024 18:40:34 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1-20`

```console
$ docker pull mongo-express@sha256:f7326dae3fccd7fb5070f0a662462c64e01edb16bb9306d9e740ea7ba6151508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1-20` - linux; amd64

```console
$ docker pull mongo-express@sha256:885763f82abcd39c6486a03f0c3f9d54a4f8e92fcc3468fcfa17c4fae28efa01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81657401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7971232360c00df0c9656b9707da864e1c363804a7a790c4c27280ee958277c`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 22:20:35 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 22:20:44 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 22:20:44 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 22:20:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 22:20:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 22:20:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 22:20:51 GMT
CMD ["node"]
# Wed, 10 Jan 2024 22:46:39 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 22:46:39 GMT
WORKDIR /app
# Wed, 10 Jan 2024 22:46:39 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 22:46:39 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 22:47:17 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:30 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:30 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:30 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:30 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:30 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c5cc2f8656f55dc78885a03f73843da455fff1c91cc918c9911a22da86c85f`  
		Last Modified: Wed, 10 Jan 2024 22:26:36 GMT  
		Size: 42.0 MB (42048744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006469274c1580679dfd80bae2ac29ad79f987d8e2ed544ef6fbb94ea6e65cd4`  
		Last Modified: Wed, 10 Jan 2024 22:26:30 GMT  
		Size: 2.3 MB (2341030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0abed5da9c630045ae1895626d1acb1bf0100f5b9fd0aea9f10dd40e8e5ddb0`  
		Last Modified: Wed, 10 Jan 2024 22:26:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3df57b3cbcf09a78321bada9c4605a5233dcb9d430f725e2860e710e4b8258`  
		Last Modified: Wed, 10 Jan 2024 22:48:03 GMT  
		Size: 802.3 KB (802313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac5f95f60b6e09b1b872314f803e877023ee41bb642656c36e75fb9c30b45c1`  
		Last Modified: Wed, 10 Jan 2024 22:48:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dafb24b4ba1a0e51191aa8847da705219b97a02bdfc80f46eaeefc317af57f7`  
		Last Modified: Wed, 10 Jan 2024 22:48:10 GMT  
		Size: 33.1 MB (33061463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758d7c0911e9e5f682a3b7829e9b7bf764032efb69ef12892204a17ead497716`  
		Last Modified: Tue, 16 Jan 2024 18:34:08 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1-20` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:7fe75277ae7ceefa1112a1f43d34739b860560e1be4c353fc29e29bd6d28948a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81431703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80adae553b99768fc4e99a45894ff0cfba5c7d721e88978fbe041b333b6e60a0`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 22:40:02 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 23:04:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 23:04:07 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 23:04:12 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 23:04:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 23:04:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 23:04:12 GMT
CMD ["node"]
# Wed, 10 Jan 2024 23:52:02 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 23:52:02 GMT
WORKDIR /app
# Wed, 10 Jan 2024 23:52:02 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 23:52:02 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 23:52:33 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:46 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:46 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:46 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:46 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:46 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c70dab0f60cbd7ad10095fec2d98dbad870982c1eed23fa6935412a3df1deb6`  
		Last Modified: Wed, 10 Jan 2024 23:32:52 GMT  
		Size: 41.8 MB (41807939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdf0c1dda85712846cb5694ff5531d1c12b10ec91363e5b3bed06fe8252cade`  
		Last Modified: Wed, 10 Jan 2024 23:32:48 GMT  
		Size: 2.3 MB (2341034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2395c944a99ad0901490abcadc8fcd4e1c5844aa4a8dd8f79db7364671c2f09`  
		Last Modified: Wed, 10 Jan 2024 23:32:47 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05efae4c9e725aab673bf0c595a3764e030e18b5f647d1cdd21eacbe2ba416e8`  
		Last Modified: Wed, 10 Jan 2024 23:53:13 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc512d7f9664d62415473b446e2c5be04fc1e8649473aed59af75fdd33bc154`  
		Last Modified: Wed, 10 Jan 2024 23:53:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a46081d56efdee0b4b719f3ebfbd90c14ac66148258d240816732e892f5e567`  
		Last Modified: Wed, 10 Jan 2024 23:53:19 GMT  
		Size: 33.1 MB (33061276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c151290e103ea7259c94eabc14a4eb58f0940c59479b1a74294dbaa1afefe6`  
		Last Modified: Tue, 16 Jan 2024 18:40:18 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1-20-alpine3.18`

```console
$ docker pull mongo-express@sha256:f7326dae3fccd7fb5070f0a662462c64e01edb16bb9306d9e740ea7ba6151508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1-20-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:885763f82abcd39c6486a03f0c3f9d54a4f8e92fcc3468fcfa17c4fae28efa01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81657401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7971232360c00df0c9656b9707da864e1c363804a7a790c4c27280ee958277c`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 22:20:35 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 22:20:44 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 22:20:44 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 22:20:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 22:20:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 22:20:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 22:20:51 GMT
CMD ["node"]
# Wed, 10 Jan 2024 22:46:39 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 22:46:39 GMT
WORKDIR /app
# Wed, 10 Jan 2024 22:46:39 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 22:46:39 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 22:47:17 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:30 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:30 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:30 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:30 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:30 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c5cc2f8656f55dc78885a03f73843da455fff1c91cc918c9911a22da86c85f`  
		Last Modified: Wed, 10 Jan 2024 22:26:36 GMT  
		Size: 42.0 MB (42048744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006469274c1580679dfd80bae2ac29ad79f987d8e2ed544ef6fbb94ea6e65cd4`  
		Last Modified: Wed, 10 Jan 2024 22:26:30 GMT  
		Size: 2.3 MB (2341030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0abed5da9c630045ae1895626d1acb1bf0100f5b9fd0aea9f10dd40e8e5ddb0`  
		Last Modified: Wed, 10 Jan 2024 22:26:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3df57b3cbcf09a78321bada9c4605a5233dcb9d430f725e2860e710e4b8258`  
		Last Modified: Wed, 10 Jan 2024 22:48:03 GMT  
		Size: 802.3 KB (802313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac5f95f60b6e09b1b872314f803e877023ee41bb642656c36e75fb9c30b45c1`  
		Last Modified: Wed, 10 Jan 2024 22:48:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dafb24b4ba1a0e51191aa8847da705219b97a02bdfc80f46eaeefc317af57f7`  
		Last Modified: Wed, 10 Jan 2024 22:48:10 GMT  
		Size: 33.1 MB (33061463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758d7c0911e9e5f682a3b7829e9b7bf764032efb69ef12892204a17ead497716`  
		Last Modified: Tue, 16 Jan 2024 18:34:08 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1-20-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:7fe75277ae7ceefa1112a1f43d34739b860560e1be4c353fc29e29bd6d28948a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81431703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80adae553b99768fc4e99a45894ff0cfba5c7d721e88978fbe041b333b6e60a0`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 22:40:02 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 23:04:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 23:04:07 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 23:04:12 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 23:04:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 23:04:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 23:04:12 GMT
CMD ["node"]
# Wed, 10 Jan 2024 23:52:02 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 23:52:02 GMT
WORKDIR /app
# Wed, 10 Jan 2024 23:52:02 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 23:52:02 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 23:52:33 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:46 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:46 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:46 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:46 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:46 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c70dab0f60cbd7ad10095fec2d98dbad870982c1eed23fa6935412a3df1deb6`  
		Last Modified: Wed, 10 Jan 2024 23:32:52 GMT  
		Size: 41.8 MB (41807939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdf0c1dda85712846cb5694ff5531d1c12b10ec91363e5b3bed06fe8252cade`  
		Last Modified: Wed, 10 Jan 2024 23:32:48 GMT  
		Size: 2.3 MB (2341034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2395c944a99ad0901490abcadc8fcd4e1c5844aa4a8dd8f79db7364671c2f09`  
		Last Modified: Wed, 10 Jan 2024 23:32:47 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05efae4c9e725aab673bf0c595a3764e030e18b5f647d1cdd21eacbe2ba416e8`  
		Last Modified: Wed, 10 Jan 2024 23:53:13 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc512d7f9664d62415473b446e2c5be04fc1e8649473aed59af75fdd33bc154`  
		Last Modified: Wed, 10 Jan 2024 23:53:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a46081d56efdee0b4b719f3ebfbd90c14ac66148258d240816732e892f5e567`  
		Last Modified: Wed, 10 Jan 2024 23:53:19 GMT  
		Size: 33.1 MB (33061276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c151290e103ea7259c94eabc14a4eb58f0940c59479b1a74294dbaa1afefe6`  
		Last Modified: Tue, 16 Jan 2024 18:40:18 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1-20-alpine3.19`

```console
$ docker pull mongo-express@sha256:65f053960cdc0b512ca9b0ca38ac66ddf79da9e17a55e0bb6f67ee429b87aca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1-20-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:f073fe32e107c98acd895b93b5021b98c22fc5073eae662c5b123b80947415ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81764461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a98c1a3f58478f695597e44f0cdb4f09f8561a93ad6df3181949e73cd19b53`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 22:20:56 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 22:21:04 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 22:21:05 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 22:21:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 22:21:10 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 22:21:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 22:21:10 GMT
CMD ["node"]
# Wed, 10 Jan 2024 22:45:50 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 22:45:50 GMT
WORKDIR /app
# Wed, 10 Jan 2024 22:45:50 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 22:45:50 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 22:46:28 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:27 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:27 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:27 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:27 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:27 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be93293fd5362dfcc94826d8bd1f36150cb06ed2ed085d21d9dba20195faded7`  
		Last Modified: Wed, 10 Jan 2024 22:26:57 GMT  
		Size: 42.2 MB (42167339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376f9b7a67706b1a26941e182521e904295efb7b090d524a191417621d70d0db`  
		Last Modified: Wed, 10 Jan 2024 22:26:51 GMT  
		Size: 2.3 MB (2340977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e53c60b2bbe88730ffe3d177c7169bd98e824643e5f9fa3f2656e67725b35f5`  
		Last Modified: Wed, 10 Jan 2024 22:26:51 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ddba759d2d86f589c939f166c9e7785bfde0ad13339103a2baf045b8c65f82e`  
		Last Modified: Wed, 10 Jan 2024 22:47:44 GMT  
		Size: 784.7 KB (784693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a948b8e0cfe41ee16ce54ad2379081adab071f8072a1c88b0bb4e5d583a2488`  
		Last Modified: Wed, 10 Jan 2024 22:47:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dfe75b5784c4893073cb269ad92e672f447fffe9665a7806f5eef05182fcc3`  
		Last Modified: Wed, 10 Jan 2024 22:47:52 GMT  
		Size: 33.1 MB (33061544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df36fcf5d731bf74001ef6bbf1938576595ca763950a95dae8ff8293bd8e131`  
		Last Modified: Tue, 16 Jan 2024 18:33:54 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1-20-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:1d8bdc2c5611867de62b9065ea15a8971ab63b4340a3902e24370f1fa6bbd6d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81624064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6e148ac6000b03eecc31b870a3940cbe6f080daf808742b028ccc2c0fac042`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 23:04:26 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 23:27:39 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 23:27:39 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 23:27:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 23:27:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 23:27:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 23:27:45 GMT
CMD ["node"]
# Wed, 10 Jan 2024 23:51:22 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 23:51:22 GMT
WORKDIR /app
# Wed, 10 Jan 2024 23:51:22 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 23:51:22 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 23:51:57 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:44 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:44 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:44 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:44 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:44 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec53874fe288a72a8b7207e1695ec626ea0bc80a7c3fa3e872c694d1605add7`  
		Last Modified: Wed, 10 Jan 2024 23:33:12 GMT  
		Size: 42.0 MB (42010031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3946ff1ba9858829b3ccbb2f4b3e06515829d3847659ea96287591a76801fe29`  
		Last Modified: Wed, 10 Jan 2024 23:33:08 GMT  
		Size: 2.3 MB (2341097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2987d39b19e8c4f23a1841693e2ea0b850c3817af22d9a0623b2c9c351ef8b`  
		Last Modified: Wed, 10 Jan 2024 23:33:07 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75da99a625c30c70eb981856dd368a287a882717ea69362ccca1b67e03df34e1`  
		Last Modified: Wed, 10 Jan 2024 23:52:56 GMT  
		Size: 862.4 KB (862430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5b244dd2e8846301eca1dcfe6c573ddb6fccf80eef605bbf1712ada2a3e94e`  
		Last Modified: Wed, 10 Jan 2024 23:52:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7e8f1e56d4230365fce75aaf2cd1434d33278b700dac9419a17918437c4b93`  
		Last Modified: Wed, 10 Jan 2024 23:53:02 GMT  
		Size: 33.1 MB (33061288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dc3b5f41472b90f22cb37f290027e2e2588f82d5fdbcdc51dc1b9b5ad2a4bc`  
		Last Modified: Tue, 16 Jan 2024 18:40:08 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0`

```console
$ docker pull mongo-express@sha256:98ad29b0d7cbeeba8f4640cdcd11e097081ed0ca27c89b4ee0cde63e3bfe53f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0` - linux; amd64

```console
$ docker pull mongo-express@sha256:0cba5f35c950762b9093da01ae48c19e3088093eeef8cb119529fb298685552d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79724504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d527c213d73e59c6dcc7e8b090002a1f81503a790d78d47b34df8586ce8c252f`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 01:26:35 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 01:26:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 01:26:44 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 01:26:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 01:26:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 01:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 01:26:48 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:16:13 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:16:13 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:16:52 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:37 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:37 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:37 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:37 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:37 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7465dc4da3894941da9beb13e53fea672b4167e0031a049feea4cd6ed2cd79`  
		Last Modified: Sat, 02 Dec 2023 01:34:45 GMT  
		Size: 40.1 MB (40112458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7b2bf3cf64fb3d50ff099853b0df6438ea6163f4d9d2a7880856bd36a59ba2`  
		Last Modified: Sat, 02 Dec 2023 01:34:40 GMT  
		Size: 2.3 MB (2342890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3604fe7c8f3c53b8058f060dce2cfe269aad37881cabc3fa7b88c926470e9488`  
		Last Modified: Sat, 02 Dec 2023 01:34:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef732f87d67b9f901f90ed568ca4b4cea78c7d2a37219f3a6e76d7cc2d7a75cd`  
		Last Modified: Sat, 06 Jan 2024 01:18:28 GMT  
		Size: 802.3 KB (802311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2ade8248554eb9e4592da34eccdc1e3b1097a8d22046f414f26b3ebf05d2b0`  
		Last Modified: Sat, 06 Jan 2024 01:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bb6e5f1580826a520151543dc3f7e3e536b326b7aa1e21ef81ce4480e08f4c`  
		Last Modified: Sat, 06 Jan 2024 01:18:36 GMT  
		Size: 33.1 MB (33062997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b209d7438a256fbd0fdaf2e7fb7d233773023b8019b2928737937d51026977`  
		Last Modified: Tue, 16 Jan 2024 18:34:34 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:a6846e70e124e9567bf389cf03d48b675f936ced5e4c0b65870cbe7062318a3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79444186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b30b6db7b34865b6126fd73f277de5fb3c193570fd3243921d7da8d63554c9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 03:48:51 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 04:09:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 04:09:30 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 04:09:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 04:09:35 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 04:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 04:09:35 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:56:27 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:56:27 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:56:59 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:50 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:50 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:50 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:50 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:50 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9cba98305bbc9b5b1acc82808c97ec2f1bdd0918782e26a4f249c89e8f5f1c`  
		Last Modified: Sat, 02 Dec 2023 04:17:12 GMT  
		Size: 39.8 MB (39817628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb1cdcfb3b6e7d1dbbdde57709e15e2c4bbdcac8f7c3da88459d74bc402c637`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 2.3 MB (2342686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266cff88a90930625e27a71f05f05b0bb69c1c3612e447e70131636367599c6c`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b233574749281abc1a8ad5a8fb4f54bd3aa2b79c58bd876195c947c20d3083fa`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 887.0 KB (886996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1254cb9a9f437dc36f890b22f67330bfbc4c76a86d4e1c845d093039c3455c1e`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca088f0889c67078200ebc911786a79a006f465a4c1e1a6fe630152a483e40bb`  
		Last Modified: Sat, 06 Jan 2024 01:58:29 GMT  
		Size: 33.1 MB (33062417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38362c10b0ee09dc1483616bb584925ef66302ceff20e0096c75f82025ca5fe`  
		Last Modified: Tue, 16 Jan 2024 18:40:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0-18`

```console
$ docker pull mongo-express@sha256:98ad29b0d7cbeeba8f4640cdcd11e097081ed0ca27c89b4ee0cde63e3bfe53f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0-18` - linux; amd64

```console
$ docker pull mongo-express@sha256:0cba5f35c950762b9093da01ae48c19e3088093eeef8cb119529fb298685552d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79724504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d527c213d73e59c6dcc7e8b090002a1f81503a790d78d47b34df8586ce8c252f`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 01:26:35 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 01:26:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 01:26:44 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 01:26:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 01:26:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 01:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 01:26:48 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:16:13 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:16:13 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:16:52 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:37 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:37 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:37 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:37 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:37 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7465dc4da3894941da9beb13e53fea672b4167e0031a049feea4cd6ed2cd79`  
		Last Modified: Sat, 02 Dec 2023 01:34:45 GMT  
		Size: 40.1 MB (40112458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7b2bf3cf64fb3d50ff099853b0df6438ea6163f4d9d2a7880856bd36a59ba2`  
		Last Modified: Sat, 02 Dec 2023 01:34:40 GMT  
		Size: 2.3 MB (2342890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3604fe7c8f3c53b8058f060dce2cfe269aad37881cabc3fa7b88c926470e9488`  
		Last Modified: Sat, 02 Dec 2023 01:34:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef732f87d67b9f901f90ed568ca4b4cea78c7d2a37219f3a6e76d7cc2d7a75cd`  
		Last Modified: Sat, 06 Jan 2024 01:18:28 GMT  
		Size: 802.3 KB (802311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2ade8248554eb9e4592da34eccdc1e3b1097a8d22046f414f26b3ebf05d2b0`  
		Last Modified: Sat, 06 Jan 2024 01:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bb6e5f1580826a520151543dc3f7e3e536b326b7aa1e21ef81ce4480e08f4c`  
		Last Modified: Sat, 06 Jan 2024 01:18:36 GMT  
		Size: 33.1 MB (33062997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b209d7438a256fbd0fdaf2e7fb7d233773023b8019b2928737937d51026977`  
		Last Modified: Tue, 16 Jan 2024 18:34:34 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0-18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:a6846e70e124e9567bf389cf03d48b675f936ced5e4c0b65870cbe7062318a3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79444186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b30b6db7b34865b6126fd73f277de5fb3c193570fd3243921d7da8d63554c9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 03:48:51 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 04:09:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 04:09:30 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 04:09:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 04:09:35 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 04:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 04:09:35 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:56:27 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:56:27 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:56:59 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:50 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:50 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:50 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:50 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:50 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9cba98305bbc9b5b1acc82808c97ec2f1bdd0918782e26a4f249c89e8f5f1c`  
		Last Modified: Sat, 02 Dec 2023 04:17:12 GMT  
		Size: 39.8 MB (39817628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb1cdcfb3b6e7d1dbbdde57709e15e2c4bbdcac8f7c3da88459d74bc402c637`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 2.3 MB (2342686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266cff88a90930625e27a71f05f05b0bb69c1c3612e447e70131636367599c6c`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b233574749281abc1a8ad5a8fb4f54bd3aa2b79c58bd876195c947c20d3083fa`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 887.0 KB (886996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1254cb9a9f437dc36f890b22f67330bfbc4c76a86d4e1c845d093039c3455c1e`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca088f0889c67078200ebc911786a79a006f465a4c1e1a6fe630152a483e40bb`  
		Last Modified: Sat, 06 Jan 2024 01:58:29 GMT  
		Size: 33.1 MB (33062417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38362c10b0ee09dc1483616bb584925ef66302ceff20e0096c75f82025ca5fe`  
		Last Modified: Tue, 16 Jan 2024 18:40:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0-18-alpine3.18`

```console
$ docker pull mongo-express@sha256:98ad29b0d7cbeeba8f4640cdcd11e097081ed0ca27c89b4ee0cde63e3bfe53f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0-18-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:0cba5f35c950762b9093da01ae48c19e3088093eeef8cb119529fb298685552d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79724504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d527c213d73e59c6dcc7e8b090002a1f81503a790d78d47b34df8586ce8c252f`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 01:26:35 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 01:26:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 01:26:44 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 01:26:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 01:26:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 01:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 01:26:48 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:16:13 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:16:13 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:16:52 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:37 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:37 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:37 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:37 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:37 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7465dc4da3894941da9beb13e53fea672b4167e0031a049feea4cd6ed2cd79`  
		Last Modified: Sat, 02 Dec 2023 01:34:45 GMT  
		Size: 40.1 MB (40112458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7b2bf3cf64fb3d50ff099853b0df6438ea6163f4d9d2a7880856bd36a59ba2`  
		Last Modified: Sat, 02 Dec 2023 01:34:40 GMT  
		Size: 2.3 MB (2342890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3604fe7c8f3c53b8058f060dce2cfe269aad37881cabc3fa7b88c926470e9488`  
		Last Modified: Sat, 02 Dec 2023 01:34:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef732f87d67b9f901f90ed568ca4b4cea78c7d2a37219f3a6e76d7cc2d7a75cd`  
		Last Modified: Sat, 06 Jan 2024 01:18:28 GMT  
		Size: 802.3 KB (802311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2ade8248554eb9e4592da34eccdc1e3b1097a8d22046f414f26b3ebf05d2b0`  
		Last Modified: Sat, 06 Jan 2024 01:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bb6e5f1580826a520151543dc3f7e3e536b326b7aa1e21ef81ce4480e08f4c`  
		Last Modified: Sat, 06 Jan 2024 01:18:36 GMT  
		Size: 33.1 MB (33062997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b209d7438a256fbd0fdaf2e7fb7d233773023b8019b2928737937d51026977`  
		Last Modified: Tue, 16 Jan 2024 18:34:34 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0-18-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:a6846e70e124e9567bf389cf03d48b675f936ced5e4c0b65870cbe7062318a3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79444186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b30b6db7b34865b6126fd73f277de5fb3c193570fd3243921d7da8d63554c9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 03:48:51 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 04:09:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 04:09:30 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 04:09:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 04:09:35 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 04:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 04:09:35 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:56:27 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:56:27 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:56:59 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:50 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:50 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:50 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:50 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:50 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9cba98305bbc9b5b1acc82808c97ec2f1bdd0918782e26a4f249c89e8f5f1c`  
		Last Modified: Sat, 02 Dec 2023 04:17:12 GMT  
		Size: 39.8 MB (39817628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb1cdcfb3b6e7d1dbbdde57709e15e2c4bbdcac8f7c3da88459d74bc402c637`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 2.3 MB (2342686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266cff88a90930625e27a71f05f05b0bb69c1c3612e447e70131636367599c6c`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b233574749281abc1a8ad5a8fb4f54bd3aa2b79c58bd876195c947c20d3083fa`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 887.0 KB (886996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1254cb9a9f437dc36f890b22f67330bfbc4c76a86d4e1c845d093039c3455c1e`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca088f0889c67078200ebc911786a79a006f465a4c1e1a6fe630152a483e40bb`  
		Last Modified: Sat, 06 Jan 2024 01:58:29 GMT  
		Size: 33.1 MB (33062417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38362c10b0ee09dc1483616bb584925ef66302ceff20e0096c75f82025ca5fe`  
		Last Modified: Tue, 16 Jan 2024 18:40:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0-18-alpine3.19`

```console
$ docker pull mongo-express@sha256:78bdf802ed37afc5a00c0689938a05c07eb0c044f5b78943cd01810892bc7165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0-18-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:76b2b013b8a9645dbe3ba2c1ce248ed227e1cd4f08a733f45f296565b8a9f8cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79837273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4579ff05115b2d8f428c5c77751ac90df4365faa4ad99f6686d11990a1f8f6f8`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Mon, 11 Dec 2023 18:37:13 GMT
ENV NODE_VERSION=18.19.0
# Mon, 11 Dec 2023 18:37:21 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Mon, 11 Dec 2023 18:37:22 GMT
ENV YARN_VERSION=1.22.19
# Mon, 11 Dec 2023 18:37:26 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 11 Dec 2023 18:37:26 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 11 Dec 2023 18:37:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Dec 2023 18:37:26 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:15:24 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:15:25 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:15:25 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:15:25 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:16:03 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:33 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:33 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:34 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:34 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:34 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f158788f409a5decd9495205daf4aa17df26d8219d6dc12acab5949342866fe`  
		Last Modified: Mon, 11 Dec 2023 18:40:25 GMT  
		Size: 40.2 MB (40236806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f028dff98271801e449c3ebac94a319851128c0ec687e13e00a68b2d98ec4700`  
		Last Modified: Mon, 11 Dec 2023 18:40:20 GMT  
		Size: 2.3 MB (2342755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f25c33705ddc3351cc4893fdc0a38405bdd0741643798918fa2b0146fd5a9d`  
		Last Modified: Mon, 11 Dec 2023 18:40:20 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fda4c5ad911063ff2d7ecb2537ab17e4c64d8b807138529677046ad06658793`  
		Last Modified: Sat, 06 Jan 2024 01:18:07 GMT  
		Size: 784.7 KB (784696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305d1a20d5027c21e855e059ee3b955582ec8dfe68e68216840344bbb4044e8f`  
		Last Modified: Sat, 06 Jan 2024 01:18:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d135d844ee3fac33c4b754dd160f532b303ec6d2dc049881149fb27b560663c`  
		Last Modified: Sat, 06 Jan 2024 01:18:15 GMT  
		Size: 33.1 MB (33063111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a1ca949f7cf2b0d7454dfddf692b268ba94311f570c0e5020a9ccda85718bf`  
		Last Modified: Tue, 16 Jan 2024 18:34:24 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0-18-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:b2d2b5a4d1d9b6ab5237ff3bdbbc30682d7c3f4c0569465d994e9f9221e02444
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79595014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76484dd7c6136aa629ff8682f1a65e3203c853cb75d602cbeea8c37f4417c31f`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Mon, 11 Dec 2023 18:40:05 GMT
ENV NODE_VERSION=18.19.0
# Mon, 11 Dec 2023 18:59:50 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Mon, 11 Dec 2023 18:59:50 GMT
ENV YARN_VERSION=1.22.19
# Mon, 11 Dec 2023 18:59:55 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 11 Dec 2023 18:59:55 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 11 Dec 2023 18:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Dec 2023 18:59:55 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:55:47 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:55:47 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:55:47 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:55:47 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:56:19 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:48 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:48 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:48 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:48 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:48 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7895eb72c1a145d166631d5a81c61bffd747783c52e8a1de9fa0e7d5871817`  
		Last Modified: Mon, 11 Dec 2023 19:02:51 GMT  
		Size: 40.0 MB (39978047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7049a133eb54d652049fa44657d24cef7298dc371ffab6e27f5cd5e53e62159f`  
		Last Modified: Mon, 11 Dec 2023 19:02:46 GMT  
		Size: 2.3 MB (2342730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90577567f13c6046278cbfa4a557cb5a19ed5f9c281ab540e84ddd8f74c71922`  
		Last Modified: Mon, 11 Dec 2023 19:02:45 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7fdab078a277850d97a71a23c41cbf45e5ac8092bc99a1429aa8247527f598`  
		Last Modified: Sat, 06 Jan 2024 01:58:06 GMT  
		Size: 862.4 KB (862441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1063d3ecd5c04feb20d959e43633106ee5d678f9e00be9c39fb4023bf1cffb35`  
		Last Modified: Sat, 06 Jan 2024 01:58:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dea9015fc2c949ef2ca11d0fffd8f60b647169e36e2e19d01045a8716ccec2`  
		Last Modified: Sat, 06 Jan 2024 01:58:12 GMT  
		Size: 33.1 MB (33062580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e762f944899eedd67688d768a6641886edc4c56739ac72560b5471ce8ad13c70`  
		Last Modified: Tue, 16 Jan 2024 18:40:34 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0-20`

```console
$ docker pull mongo-express@sha256:f7326dae3fccd7fb5070f0a662462c64e01edb16bb9306d9e740ea7ba6151508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0-20` - linux; amd64

```console
$ docker pull mongo-express@sha256:885763f82abcd39c6486a03f0c3f9d54a4f8e92fcc3468fcfa17c4fae28efa01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81657401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7971232360c00df0c9656b9707da864e1c363804a7a790c4c27280ee958277c`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 22:20:35 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 22:20:44 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 22:20:44 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 22:20:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 22:20:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 22:20:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 22:20:51 GMT
CMD ["node"]
# Wed, 10 Jan 2024 22:46:39 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 22:46:39 GMT
WORKDIR /app
# Wed, 10 Jan 2024 22:46:39 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 22:46:39 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 22:47:17 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:30 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:30 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:30 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:30 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:30 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c5cc2f8656f55dc78885a03f73843da455fff1c91cc918c9911a22da86c85f`  
		Last Modified: Wed, 10 Jan 2024 22:26:36 GMT  
		Size: 42.0 MB (42048744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006469274c1580679dfd80bae2ac29ad79f987d8e2ed544ef6fbb94ea6e65cd4`  
		Last Modified: Wed, 10 Jan 2024 22:26:30 GMT  
		Size: 2.3 MB (2341030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0abed5da9c630045ae1895626d1acb1bf0100f5b9fd0aea9f10dd40e8e5ddb0`  
		Last Modified: Wed, 10 Jan 2024 22:26:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3df57b3cbcf09a78321bada9c4605a5233dcb9d430f725e2860e710e4b8258`  
		Last Modified: Wed, 10 Jan 2024 22:48:03 GMT  
		Size: 802.3 KB (802313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac5f95f60b6e09b1b872314f803e877023ee41bb642656c36e75fb9c30b45c1`  
		Last Modified: Wed, 10 Jan 2024 22:48:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dafb24b4ba1a0e51191aa8847da705219b97a02bdfc80f46eaeefc317af57f7`  
		Last Modified: Wed, 10 Jan 2024 22:48:10 GMT  
		Size: 33.1 MB (33061463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758d7c0911e9e5f682a3b7829e9b7bf764032efb69ef12892204a17ead497716`  
		Last Modified: Tue, 16 Jan 2024 18:34:08 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0-20` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:7fe75277ae7ceefa1112a1f43d34739b860560e1be4c353fc29e29bd6d28948a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81431703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80adae553b99768fc4e99a45894ff0cfba5c7d721e88978fbe041b333b6e60a0`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 22:40:02 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 23:04:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 23:04:07 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 23:04:12 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 23:04:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 23:04:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 23:04:12 GMT
CMD ["node"]
# Wed, 10 Jan 2024 23:52:02 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 23:52:02 GMT
WORKDIR /app
# Wed, 10 Jan 2024 23:52:02 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 23:52:02 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 23:52:33 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:46 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:46 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:46 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:46 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:46 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c70dab0f60cbd7ad10095fec2d98dbad870982c1eed23fa6935412a3df1deb6`  
		Last Modified: Wed, 10 Jan 2024 23:32:52 GMT  
		Size: 41.8 MB (41807939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdf0c1dda85712846cb5694ff5531d1c12b10ec91363e5b3bed06fe8252cade`  
		Last Modified: Wed, 10 Jan 2024 23:32:48 GMT  
		Size: 2.3 MB (2341034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2395c944a99ad0901490abcadc8fcd4e1c5844aa4a8dd8f79db7364671c2f09`  
		Last Modified: Wed, 10 Jan 2024 23:32:47 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05efae4c9e725aab673bf0c595a3764e030e18b5f647d1cdd21eacbe2ba416e8`  
		Last Modified: Wed, 10 Jan 2024 23:53:13 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc512d7f9664d62415473b446e2c5be04fc1e8649473aed59af75fdd33bc154`  
		Last Modified: Wed, 10 Jan 2024 23:53:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a46081d56efdee0b4b719f3ebfbd90c14ac66148258d240816732e892f5e567`  
		Last Modified: Wed, 10 Jan 2024 23:53:19 GMT  
		Size: 33.1 MB (33061276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c151290e103ea7259c94eabc14a4eb58f0940c59479b1a74294dbaa1afefe6`  
		Last Modified: Tue, 16 Jan 2024 18:40:18 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0-20-alpine3.18`

```console
$ docker pull mongo-express@sha256:f7326dae3fccd7fb5070f0a662462c64e01edb16bb9306d9e740ea7ba6151508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0-20-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:885763f82abcd39c6486a03f0c3f9d54a4f8e92fcc3468fcfa17c4fae28efa01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81657401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7971232360c00df0c9656b9707da864e1c363804a7a790c4c27280ee958277c`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 22:20:35 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 22:20:44 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 22:20:44 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 22:20:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 22:20:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 22:20:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 22:20:51 GMT
CMD ["node"]
# Wed, 10 Jan 2024 22:46:39 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 22:46:39 GMT
WORKDIR /app
# Wed, 10 Jan 2024 22:46:39 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 22:46:39 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 22:47:17 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:30 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:30 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:30 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:30 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:30 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c5cc2f8656f55dc78885a03f73843da455fff1c91cc918c9911a22da86c85f`  
		Last Modified: Wed, 10 Jan 2024 22:26:36 GMT  
		Size: 42.0 MB (42048744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006469274c1580679dfd80bae2ac29ad79f987d8e2ed544ef6fbb94ea6e65cd4`  
		Last Modified: Wed, 10 Jan 2024 22:26:30 GMT  
		Size: 2.3 MB (2341030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0abed5da9c630045ae1895626d1acb1bf0100f5b9fd0aea9f10dd40e8e5ddb0`  
		Last Modified: Wed, 10 Jan 2024 22:26:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3df57b3cbcf09a78321bada9c4605a5233dcb9d430f725e2860e710e4b8258`  
		Last Modified: Wed, 10 Jan 2024 22:48:03 GMT  
		Size: 802.3 KB (802313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac5f95f60b6e09b1b872314f803e877023ee41bb642656c36e75fb9c30b45c1`  
		Last Modified: Wed, 10 Jan 2024 22:48:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dafb24b4ba1a0e51191aa8847da705219b97a02bdfc80f46eaeefc317af57f7`  
		Last Modified: Wed, 10 Jan 2024 22:48:10 GMT  
		Size: 33.1 MB (33061463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758d7c0911e9e5f682a3b7829e9b7bf764032efb69ef12892204a17ead497716`  
		Last Modified: Tue, 16 Jan 2024 18:34:08 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0-20-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:7fe75277ae7ceefa1112a1f43d34739b860560e1be4c353fc29e29bd6d28948a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81431703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80adae553b99768fc4e99a45894ff0cfba5c7d721e88978fbe041b333b6e60a0`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 22:40:02 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 23:04:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 23:04:07 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 23:04:12 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 23:04:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 23:04:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 23:04:12 GMT
CMD ["node"]
# Wed, 10 Jan 2024 23:52:02 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 23:52:02 GMT
WORKDIR /app
# Wed, 10 Jan 2024 23:52:02 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 23:52:02 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 23:52:33 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:46 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:46 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:46 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:46 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:46 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c70dab0f60cbd7ad10095fec2d98dbad870982c1eed23fa6935412a3df1deb6`  
		Last Modified: Wed, 10 Jan 2024 23:32:52 GMT  
		Size: 41.8 MB (41807939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdf0c1dda85712846cb5694ff5531d1c12b10ec91363e5b3bed06fe8252cade`  
		Last Modified: Wed, 10 Jan 2024 23:32:48 GMT  
		Size: 2.3 MB (2341034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2395c944a99ad0901490abcadc8fcd4e1c5844aa4a8dd8f79db7364671c2f09`  
		Last Modified: Wed, 10 Jan 2024 23:32:47 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05efae4c9e725aab673bf0c595a3764e030e18b5f647d1cdd21eacbe2ba416e8`  
		Last Modified: Wed, 10 Jan 2024 23:53:13 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc512d7f9664d62415473b446e2c5be04fc1e8649473aed59af75fdd33bc154`  
		Last Modified: Wed, 10 Jan 2024 23:53:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a46081d56efdee0b4b719f3ebfbd90c14ac66148258d240816732e892f5e567`  
		Last Modified: Wed, 10 Jan 2024 23:53:19 GMT  
		Size: 33.1 MB (33061276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c151290e103ea7259c94eabc14a4eb58f0940c59479b1a74294dbaa1afefe6`  
		Last Modified: Tue, 16 Jan 2024 18:40:18 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0-20-alpine3.19`

```console
$ docker pull mongo-express@sha256:65f053960cdc0b512ca9b0ca38ac66ddf79da9e17a55e0bb6f67ee429b87aca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0-20-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:f073fe32e107c98acd895b93b5021b98c22fc5073eae662c5b123b80947415ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81764461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a98c1a3f58478f695597e44f0cdb4f09f8561a93ad6df3181949e73cd19b53`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 22:20:56 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 22:21:04 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 22:21:05 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 22:21:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 22:21:10 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 22:21:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 22:21:10 GMT
CMD ["node"]
# Wed, 10 Jan 2024 22:45:50 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 22:45:50 GMT
WORKDIR /app
# Wed, 10 Jan 2024 22:45:50 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 22:45:50 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 22:46:28 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:27 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:27 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:27 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:27 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:27 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be93293fd5362dfcc94826d8bd1f36150cb06ed2ed085d21d9dba20195faded7`  
		Last Modified: Wed, 10 Jan 2024 22:26:57 GMT  
		Size: 42.2 MB (42167339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376f9b7a67706b1a26941e182521e904295efb7b090d524a191417621d70d0db`  
		Last Modified: Wed, 10 Jan 2024 22:26:51 GMT  
		Size: 2.3 MB (2340977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e53c60b2bbe88730ffe3d177c7169bd98e824643e5f9fa3f2656e67725b35f5`  
		Last Modified: Wed, 10 Jan 2024 22:26:51 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ddba759d2d86f589c939f166c9e7785bfde0ad13339103a2baf045b8c65f82e`  
		Last Modified: Wed, 10 Jan 2024 22:47:44 GMT  
		Size: 784.7 KB (784693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a948b8e0cfe41ee16ce54ad2379081adab071f8072a1c88b0bb4e5d583a2488`  
		Last Modified: Wed, 10 Jan 2024 22:47:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dfe75b5784c4893073cb269ad92e672f447fffe9665a7806f5eef05182fcc3`  
		Last Modified: Wed, 10 Jan 2024 22:47:52 GMT  
		Size: 33.1 MB (33061544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df36fcf5d731bf74001ef6bbf1938576595ca763950a95dae8ff8293bd8e131`  
		Last Modified: Tue, 16 Jan 2024 18:33:54 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0-20-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:1d8bdc2c5611867de62b9065ea15a8971ab63b4340a3902e24370f1fa6bbd6d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81624064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6e148ac6000b03eecc31b870a3940cbe6f080daf808742b028ccc2c0fac042`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 23:04:26 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 23:27:39 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 23:27:39 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 23:27:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 23:27:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 23:27:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 23:27:45 GMT
CMD ["node"]
# Wed, 10 Jan 2024 23:51:22 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 23:51:22 GMT
WORKDIR /app
# Wed, 10 Jan 2024 23:51:22 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 23:51:22 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 23:51:57 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:44 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:44 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:44 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:44 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:44 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec53874fe288a72a8b7207e1695ec626ea0bc80a7c3fa3e872c694d1605add7`  
		Last Modified: Wed, 10 Jan 2024 23:33:12 GMT  
		Size: 42.0 MB (42010031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3946ff1ba9858829b3ccbb2f4b3e06515829d3847659ea96287591a76801fe29`  
		Last Modified: Wed, 10 Jan 2024 23:33:08 GMT  
		Size: 2.3 MB (2341097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2987d39b19e8c4f23a1841693e2ea0b850c3817af22d9a0623b2c9c351ef8b`  
		Last Modified: Wed, 10 Jan 2024 23:33:07 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75da99a625c30c70eb981856dd368a287a882717ea69362ccca1b67e03df34e1`  
		Last Modified: Wed, 10 Jan 2024 23:52:56 GMT  
		Size: 862.4 KB (862430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5b244dd2e8846301eca1dcfe6c573ddb6fccf80eef605bbf1712ada2a3e94e`  
		Last Modified: Wed, 10 Jan 2024 23:52:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7e8f1e56d4230365fce75aaf2cd1434d33278b700dac9419a17918437c4b93`  
		Last Modified: Wed, 10 Jan 2024 23:53:02 GMT  
		Size: 33.1 MB (33061288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dc3b5f41472b90f22cb37f290027e2e2588f82d5fdbcdc51dc1b9b5ad2a4bc`  
		Last Modified: Tue, 16 Jan 2024 18:40:08 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.2`

```console
$ docker pull mongo-express@sha256:98ad29b0d7cbeeba8f4640cdcd11e097081ed0ca27c89b4ee0cde63e3bfe53f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.2` - linux; amd64

```console
$ docker pull mongo-express@sha256:0cba5f35c950762b9093da01ae48c19e3088093eeef8cb119529fb298685552d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79724504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d527c213d73e59c6dcc7e8b090002a1f81503a790d78d47b34df8586ce8c252f`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 01:26:35 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 01:26:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 01:26:44 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 01:26:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 01:26:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 01:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 01:26:48 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:16:13 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:16:13 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:16:52 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:37 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:37 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:37 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:37 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:37 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7465dc4da3894941da9beb13e53fea672b4167e0031a049feea4cd6ed2cd79`  
		Last Modified: Sat, 02 Dec 2023 01:34:45 GMT  
		Size: 40.1 MB (40112458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7b2bf3cf64fb3d50ff099853b0df6438ea6163f4d9d2a7880856bd36a59ba2`  
		Last Modified: Sat, 02 Dec 2023 01:34:40 GMT  
		Size: 2.3 MB (2342890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3604fe7c8f3c53b8058f060dce2cfe269aad37881cabc3fa7b88c926470e9488`  
		Last Modified: Sat, 02 Dec 2023 01:34:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef732f87d67b9f901f90ed568ca4b4cea78c7d2a37219f3a6e76d7cc2d7a75cd`  
		Last Modified: Sat, 06 Jan 2024 01:18:28 GMT  
		Size: 802.3 KB (802311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2ade8248554eb9e4592da34eccdc1e3b1097a8d22046f414f26b3ebf05d2b0`  
		Last Modified: Sat, 06 Jan 2024 01:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bb6e5f1580826a520151543dc3f7e3e536b326b7aa1e21ef81ce4480e08f4c`  
		Last Modified: Sat, 06 Jan 2024 01:18:36 GMT  
		Size: 33.1 MB (33062997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b209d7438a256fbd0fdaf2e7fb7d233773023b8019b2928737937d51026977`  
		Last Modified: Tue, 16 Jan 2024 18:34:34 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.2` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:a6846e70e124e9567bf389cf03d48b675f936ced5e4c0b65870cbe7062318a3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79444186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b30b6db7b34865b6126fd73f277de5fb3c193570fd3243921d7da8d63554c9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 03:48:51 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 04:09:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 04:09:30 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 04:09:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 04:09:35 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 04:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 04:09:35 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:56:27 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:56:27 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:56:59 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:50 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:50 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:50 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:50 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:50 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9cba98305bbc9b5b1acc82808c97ec2f1bdd0918782e26a4f249c89e8f5f1c`  
		Last Modified: Sat, 02 Dec 2023 04:17:12 GMT  
		Size: 39.8 MB (39817628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb1cdcfb3b6e7d1dbbdde57709e15e2c4bbdcac8f7c3da88459d74bc402c637`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 2.3 MB (2342686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266cff88a90930625e27a71f05f05b0bb69c1c3612e447e70131636367599c6c`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b233574749281abc1a8ad5a8fb4f54bd3aa2b79c58bd876195c947c20d3083fa`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 887.0 KB (886996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1254cb9a9f437dc36f890b22f67330bfbc4c76a86d4e1c845d093039c3455c1e`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca088f0889c67078200ebc911786a79a006f465a4c1e1a6fe630152a483e40bb`  
		Last Modified: Sat, 06 Jan 2024 01:58:29 GMT  
		Size: 33.1 MB (33062417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38362c10b0ee09dc1483616bb584925ef66302ceff20e0096c75f82025ca5fe`  
		Last Modified: Tue, 16 Jan 2024 18:40:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.2-18`

```console
$ docker pull mongo-express@sha256:98ad29b0d7cbeeba8f4640cdcd11e097081ed0ca27c89b4ee0cde63e3bfe53f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.2-18` - linux; amd64

```console
$ docker pull mongo-express@sha256:0cba5f35c950762b9093da01ae48c19e3088093eeef8cb119529fb298685552d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79724504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d527c213d73e59c6dcc7e8b090002a1f81503a790d78d47b34df8586ce8c252f`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 01:26:35 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 01:26:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 01:26:44 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 01:26:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 01:26:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 01:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 01:26:48 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:16:13 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:16:13 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:16:52 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:37 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:37 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:37 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:37 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:37 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7465dc4da3894941da9beb13e53fea672b4167e0031a049feea4cd6ed2cd79`  
		Last Modified: Sat, 02 Dec 2023 01:34:45 GMT  
		Size: 40.1 MB (40112458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7b2bf3cf64fb3d50ff099853b0df6438ea6163f4d9d2a7880856bd36a59ba2`  
		Last Modified: Sat, 02 Dec 2023 01:34:40 GMT  
		Size: 2.3 MB (2342890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3604fe7c8f3c53b8058f060dce2cfe269aad37881cabc3fa7b88c926470e9488`  
		Last Modified: Sat, 02 Dec 2023 01:34:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef732f87d67b9f901f90ed568ca4b4cea78c7d2a37219f3a6e76d7cc2d7a75cd`  
		Last Modified: Sat, 06 Jan 2024 01:18:28 GMT  
		Size: 802.3 KB (802311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2ade8248554eb9e4592da34eccdc1e3b1097a8d22046f414f26b3ebf05d2b0`  
		Last Modified: Sat, 06 Jan 2024 01:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bb6e5f1580826a520151543dc3f7e3e536b326b7aa1e21ef81ce4480e08f4c`  
		Last Modified: Sat, 06 Jan 2024 01:18:36 GMT  
		Size: 33.1 MB (33062997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b209d7438a256fbd0fdaf2e7fb7d233773023b8019b2928737937d51026977`  
		Last Modified: Tue, 16 Jan 2024 18:34:34 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.2-18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:a6846e70e124e9567bf389cf03d48b675f936ced5e4c0b65870cbe7062318a3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79444186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b30b6db7b34865b6126fd73f277de5fb3c193570fd3243921d7da8d63554c9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 03:48:51 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 04:09:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 04:09:30 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 04:09:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 04:09:35 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 04:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 04:09:35 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:56:27 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:56:27 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:56:59 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:50 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:50 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:50 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:50 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:50 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9cba98305bbc9b5b1acc82808c97ec2f1bdd0918782e26a4f249c89e8f5f1c`  
		Last Modified: Sat, 02 Dec 2023 04:17:12 GMT  
		Size: 39.8 MB (39817628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb1cdcfb3b6e7d1dbbdde57709e15e2c4bbdcac8f7c3da88459d74bc402c637`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 2.3 MB (2342686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266cff88a90930625e27a71f05f05b0bb69c1c3612e447e70131636367599c6c`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b233574749281abc1a8ad5a8fb4f54bd3aa2b79c58bd876195c947c20d3083fa`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 887.0 KB (886996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1254cb9a9f437dc36f890b22f67330bfbc4c76a86d4e1c845d093039c3455c1e`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca088f0889c67078200ebc911786a79a006f465a4c1e1a6fe630152a483e40bb`  
		Last Modified: Sat, 06 Jan 2024 01:58:29 GMT  
		Size: 33.1 MB (33062417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38362c10b0ee09dc1483616bb584925ef66302ceff20e0096c75f82025ca5fe`  
		Last Modified: Tue, 16 Jan 2024 18:40:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.2-18-alpine3.18`

```console
$ docker pull mongo-express@sha256:98ad29b0d7cbeeba8f4640cdcd11e097081ed0ca27c89b4ee0cde63e3bfe53f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.2-18-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:0cba5f35c950762b9093da01ae48c19e3088093eeef8cb119529fb298685552d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79724504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d527c213d73e59c6dcc7e8b090002a1f81503a790d78d47b34df8586ce8c252f`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 01:26:35 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 01:26:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 01:26:44 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 01:26:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 01:26:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 01:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 01:26:48 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:16:13 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:16:13 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:16:52 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:37 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:37 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:37 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:37 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:37 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7465dc4da3894941da9beb13e53fea672b4167e0031a049feea4cd6ed2cd79`  
		Last Modified: Sat, 02 Dec 2023 01:34:45 GMT  
		Size: 40.1 MB (40112458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7b2bf3cf64fb3d50ff099853b0df6438ea6163f4d9d2a7880856bd36a59ba2`  
		Last Modified: Sat, 02 Dec 2023 01:34:40 GMT  
		Size: 2.3 MB (2342890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3604fe7c8f3c53b8058f060dce2cfe269aad37881cabc3fa7b88c926470e9488`  
		Last Modified: Sat, 02 Dec 2023 01:34:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef732f87d67b9f901f90ed568ca4b4cea78c7d2a37219f3a6e76d7cc2d7a75cd`  
		Last Modified: Sat, 06 Jan 2024 01:18:28 GMT  
		Size: 802.3 KB (802311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2ade8248554eb9e4592da34eccdc1e3b1097a8d22046f414f26b3ebf05d2b0`  
		Last Modified: Sat, 06 Jan 2024 01:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bb6e5f1580826a520151543dc3f7e3e536b326b7aa1e21ef81ce4480e08f4c`  
		Last Modified: Sat, 06 Jan 2024 01:18:36 GMT  
		Size: 33.1 MB (33062997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b209d7438a256fbd0fdaf2e7fb7d233773023b8019b2928737937d51026977`  
		Last Modified: Tue, 16 Jan 2024 18:34:34 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.2-18-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:a6846e70e124e9567bf389cf03d48b675f936ced5e4c0b65870cbe7062318a3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79444186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b30b6db7b34865b6126fd73f277de5fb3c193570fd3243921d7da8d63554c9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 03:48:51 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 04:09:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 04:09:30 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 04:09:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 04:09:35 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 04:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 04:09:35 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:56:27 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:56:27 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:56:59 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:50 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:50 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:50 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:50 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:50 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9cba98305bbc9b5b1acc82808c97ec2f1bdd0918782e26a4f249c89e8f5f1c`  
		Last Modified: Sat, 02 Dec 2023 04:17:12 GMT  
		Size: 39.8 MB (39817628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb1cdcfb3b6e7d1dbbdde57709e15e2c4bbdcac8f7c3da88459d74bc402c637`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 2.3 MB (2342686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266cff88a90930625e27a71f05f05b0bb69c1c3612e447e70131636367599c6c`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b233574749281abc1a8ad5a8fb4f54bd3aa2b79c58bd876195c947c20d3083fa`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 887.0 KB (886996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1254cb9a9f437dc36f890b22f67330bfbc4c76a86d4e1c845d093039c3455c1e`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca088f0889c67078200ebc911786a79a006f465a4c1e1a6fe630152a483e40bb`  
		Last Modified: Sat, 06 Jan 2024 01:58:29 GMT  
		Size: 33.1 MB (33062417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38362c10b0ee09dc1483616bb584925ef66302ceff20e0096c75f82025ca5fe`  
		Last Modified: Tue, 16 Jan 2024 18:40:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.2-18-alpine3.19`

```console
$ docker pull mongo-express@sha256:78bdf802ed37afc5a00c0689938a05c07eb0c044f5b78943cd01810892bc7165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.2-18-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:76b2b013b8a9645dbe3ba2c1ce248ed227e1cd4f08a733f45f296565b8a9f8cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79837273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4579ff05115b2d8f428c5c77751ac90df4365faa4ad99f6686d11990a1f8f6f8`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Mon, 11 Dec 2023 18:37:13 GMT
ENV NODE_VERSION=18.19.0
# Mon, 11 Dec 2023 18:37:21 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Mon, 11 Dec 2023 18:37:22 GMT
ENV YARN_VERSION=1.22.19
# Mon, 11 Dec 2023 18:37:26 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 11 Dec 2023 18:37:26 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 11 Dec 2023 18:37:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Dec 2023 18:37:26 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:15:24 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:15:25 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:15:25 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:15:25 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:16:03 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:33 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:33 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:34 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:34 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:34 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f158788f409a5decd9495205daf4aa17df26d8219d6dc12acab5949342866fe`  
		Last Modified: Mon, 11 Dec 2023 18:40:25 GMT  
		Size: 40.2 MB (40236806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f028dff98271801e449c3ebac94a319851128c0ec687e13e00a68b2d98ec4700`  
		Last Modified: Mon, 11 Dec 2023 18:40:20 GMT  
		Size: 2.3 MB (2342755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f25c33705ddc3351cc4893fdc0a38405bdd0741643798918fa2b0146fd5a9d`  
		Last Modified: Mon, 11 Dec 2023 18:40:20 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fda4c5ad911063ff2d7ecb2537ab17e4c64d8b807138529677046ad06658793`  
		Last Modified: Sat, 06 Jan 2024 01:18:07 GMT  
		Size: 784.7 KB (784696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305d1a20d5027c21e855e059ee3b955582ec8dfe68e68216840344bbb4044e8f`  
		Last Modified: Sat, 06 Jan 2024 01:18:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d135d844ee3fac33c4b754dd160f532b303ec6d2dc049881149fb27b560663c`  
		Last Modified: Sat, 06 Jan 2024 01:18:15 GMT  
		Size: 33.1 MB (33063111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a1ca949f7cf2b0d7454dfddf692b268ba94311f570c0e5020a9ccda85718bf`  
		Last Modified: Tue, 16 Jan 2024 18:34:24 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.2-18-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:b2d2b5a4d1d9b6ab5237ff3bdbbc30682d7c3f4c0569465d994e9f9221e02444
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79595014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76484dd7c6136aa629ff8682f1a65e3203c853cb75d602cbeea8c37f4417c31f`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Mon, 11 Dec 2023 18:40:05 GMT
ENV NODE_VERSION=18.19.0
# Mon, 11 Dec 2023 18:59:50 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Mon, 11 Dec 2023 18:59:50 GMT
ENV YARN_VERSION=1.22.19
# Mon, 11 Dec 2023 18:59:55 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Mon, 11 Dec 2023 18:59:55 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Mon, 11 Dec 2023 18:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Dec 2023 18:59:55 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:55:47 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:55:47 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:55:47 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:55:47 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:56:19 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:48 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:48 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:48 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:48 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:48 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7895eb72c1a145d166631d5a81c61bffd747783c52e8a1de9fa0e7d5871817`  
		Last Modified: Mon, 11 Dec 2023 19:02:51 GMT  
		Size: 40.0 MB (39978047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7049a133eb54d652049fa44657d24cef7298dc371ffab6e27f5cd5e53e62159f`  
		Last Modified: Mon, 11 Dec 2023 19:02:46 GMT  
		Size: 2.3 MB (2342730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90577567f13c6046278cbfa4a557cb5a19ed5f9c281ab540e84ddd8f74c71922`  
		Last Modified: Mon, 11 Dec 2023 19:02:45 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7fdab078a277850d97a71a23c41cbf45e5ac8092bc99a1429aa8247527f598`  
		Last Modified: Sat, 06 Jan 2024 01:58:06 GMT  
		Size: 862.4 KB (862441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1063d3ecd5c04feb20d959e43633106ee5d678f9e00be9c39fb4023bf1cffb35`  
		Last Modified: Sat, 06 Jan 2024 01:58:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dea9015fc2c949ef2ca11d0fffd8f60b647169e36e2e19d01045a8716ccec2`  
		Last Modified: Sat, 06 Jan 2024 01:58:12 GMT  
		Size: 33.1 MB (33062580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e762f944899eedd67688d768a6641886edc4c56739ac72560b5471ce8ad13c70`  
		Last Modified: Tue, 16 Jan 2024 18:40:34 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.2-20`

```console
$ docker pull mongo-express@sha256:f7326dae3fccd7fb5070f0a662462c64e01edb16bb9306d9e740ea7ba6151508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.2-20` - linux; amd64

```console
$ docker pull mongo-express@sha256:885763f82abcd39c6486a03f0c3f9d54a4f8e92fcc3468fcfa17c4fae28efa01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81657401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7971232360c00df0c9656b9707da864e1c363804a7a790c4c27280ee958277c`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 22:20:35 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 22:20:44 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 22:20:44 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 22:20:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 22:20:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 22:20:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 22:20:51 GMT
CMD ["node"]
# Wed, 10 Jan 2024 22:46:39 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 22:46:39 GMT
WORKDIR /app
# Wed, 10 Jan 2024 22:46:39 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 22:46:39 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 22:47:17 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:30 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:30 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:30 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:30 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:30 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c5cc2f8656f55dc78885a03f73843da455fff1c91cc918c9911a22da86c85f`  
		Last Modified: Wed, 10 Jan 2024 22:26:36 GMT  
		Size: 42.0 MB (42048744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006469274c1580679dfd80bae2ac29ad79f987d8e2ed544ef6fbb94ea6e65cd4`  
		Last Modified: Wed, 10 Jan 2024 22:26:30 GMT  
		Size: 2.3 MB (2341030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0abed5da9c630045ae1895626d1acb1bf0100f5b9fd0aea9f10dd40e8e5ddb0`  
		Last Modified: Wed, 10 Jan 2024 22:26:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3df57b3cbcf09a78321bada9c4605a5233dcb9d430f725e2860e710e4b8258`  
		Last Modified: Wed, 10 Jan 2024 22:48:03 GMT  
		Size: 802.3 KB (802313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac5f95f60b6e09b1b872314f803e877023ee41bb642656c36e75fb9c30b45c1`  
		Last Modified: Wed, 10 Jan 2024 22:48:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dafb24b4ba1a0e51191aa8847da705219b97a02bdfc80f46eaeefc317af57f7`  
		Last Modified: Wed, 10 Jan 2024 22:48:10 GMT  
		Size: 33.1 MB (33061463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758d7c0911e9e5f682a3b7829e9b7bf764032efb69ef12892204a17ead497716`  
		Last Modified: Tue, 16 Jan 2024 18:34:08 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.2-20` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:7fe75277ae7ceefa1112a1f43d34739b860560e1be4c353fc29e29bd6d28948a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81431703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80adae553b99768fc4e99a45894ff0cfba5c7d721e88978fbe041b333b6e60a0`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 22:40:02 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 23:04:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 23:04:07 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 23:04:12 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 23:04:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 23:04:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 23:04:12 GMT
CMD ["node"]
# Wed, 10 Jan 2024 23:52:02 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 23:52:02 GMT
WORKDIR /app
# Wed, 10 Jan 2024 23:52:02 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 23:52:02 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 23:52:33 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:46 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:46 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:46 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:46 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:46 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c70dab0f60cbd7ad10095fec2d98dbad870982c1eed23fa6935412a3df1deb6`  
		Last Modified: Wed, 10 Jan 2024 23:32:52 GMT  
		Size: 41.8 MB (41807939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdf0c1dda85712846cb5694ff5531d1c12b10ec91363e5b3bed06fe8252cade`  
		Last Modified: Wed, 10 Jan 2024 23:32:48 GMT  
		Size: 2.3 MB (2341034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2395c944a99ad0901490abcadc8fcd4e1c5844aa4a8dd8f79db7364671c2f09`  
		Last Modified: Wed, 10 Jan 2024 23:32:47 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05efae4c9e725aab673bf0c595a3764e030e18b5f647d1cdd21eacbe2ba416e8`  
		Last Modified: Wed, 10 Jan 2024 23:53:13 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc512d7f9664d62415473b446e2c5be04fc1e8649473aed59af75fdd33bc154`  
		Last Modified: Wed, 10 Jan 2024 23:53:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a46081d56efdee0b4b719f3ebfbd90c14ac66148258d240816732e892f5e567`  
		Last Modified: Wed, 10 Jan 2024 23:53:19 GMT  
		Size: 33.1 MB (33061276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c151290e103ea7259c94eabc14a4eb58f0940c59479b1a74294dbaa1afefe6`  
		Last Modified: Tue, 16 Jan 2024 18:40:18 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.2-20-alpine3.18`

```console
$ docker pull mongo-express@sha256:f7326dae3fccd7fb5070f0a662462c64e01edb16bb9306d9e740ea7ba6151508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.2-20-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:885763f82abcd39c6486a03f0c3f9d54a4f8e92fcc3468fcfa17c4fae28efa01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81657401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7971232360c00df0c9656b9707da864e1c363804a7a790c4c27280ee958277c`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 22:20:35 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 22:20:44 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 22:20:44 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 22:20:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 22:20:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 22:20:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 22:20:51 GMT
CMD ["node"]
# Wed, 10 Jan 2024 22:46:39 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 22:46:39 GMT
WORKDIR /app
# Wed, 10 Jan 2024 22:46:39 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 22:46:39 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 22:47:17 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:30 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:30 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:30 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:30 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:30 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c5cc2f8656f55dc78885a03f73843da455fff1c91cc918c9911a22da86c85f`  
		Last Modified: Wed, 10 Jan 2024 22:26:36 GMT  
		Size: 42.0 MB (42048744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006469274c1580679dfd80bae2ac29ad79f987d8e2ed544ef6fbb94ea6e65cd4`  
		Last Modified: Wed, 10 Jan 2024 22:26:30 GMT  
		Size: 2.3 MB (2341030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0abed5da9c630045ae1895626d1acb1bf0100f5b9fd0aea9f10dd40e8e5ddb0`  
		Last Modified: Wed, 10 Jan 2024 22:26:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3df57b3cbcf09a78321bada9c4605a5233dcb9d430f725e2860e710e4b8258`  
		Last Modified: Wed, 10 Jan 2024 22:48:03 GMT  
		Size: 802.3 KB (802313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac5f95f60b6e09b1b872314f803e877023ee41bb642656c36e75fb9c30b45c1`  
		Last Modified: Wed, 10 Jan 2024 22:48:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dafb24b4ba1a0e51191aa8847da705219b97a02bdfc80f46eaeefc317af57f7`  
		Last Modified: Wed, 10 Jan 2024 22:48:10 GMT  
		Size: 33.1 MB (33061463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758d7c0911e9e5f682a3b7829e9b7bf764032efb69ef12892204a17ead497716`  
		Last Modified: Tue, 16 Jan 2024 18:34:08 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.2-20-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:7fe75277ae7ceefa1112a1f43d34739b860560e1be4c353fc29e29bd6d28948a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81431703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80adae553b99768fc4e99a45894ff0cfba5c7d721e88978fbe041b333b6e60a0`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 22:40:02 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 23:04:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 23:04:07 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 23:04:12 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 23:04:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 23:04:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 23:04:12 GMT
CMD ["node"]
# Wed, 10 Jan 2024 23:52:02 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 23:52:02 GMT
WORKDIR /app
# Wed, 10 Jan 2024 23:52:02 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 23:52:02 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 23:52:33 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:46 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:46 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:46 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:46 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:46 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c70dab0f60cbd7ad10095fec2d98dbad870982c1eed23fa6935412a3df1deb6`  
		Last Modified: Wed, 10 Jan 2024 23:32:52 GMT  
		Size: 41.8 MB (41807939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdf0c1dda85712846cb5694ff5531d1c12b10ec91363e5b3bed06fe8252cade`  
		Last Modified: Wed, 10 Jan 2024 23:32:48 GMT  
		Size: 2.3 MB (2341034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2395c944a99ad0901490abcadc8fcd4e1c5844aa4a8dd8f79db7364671c2f09`  
		Last Modified: Wed, 10 Jan 2024 23:32:47 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05efae4c9e725aab673bf0c595a3764e030e18b5f647d1cdd21eacbe2ba416e8`  
		Last Modified: Wed, 10 Jan 2024 23:53:13 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc512d7f9664d62415473b446e2c5be04fc1e8649473aed59af75fdd33bc154`  
		Last Modified: Wed, 10 Jan 2024 23:53:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a46081d56efdee0b4b719f3ebfbd90c14ac66148258d240816732e892f5e567`  
		Last Modified: Wed, 10 Jan 2024 23:53:19 GMT  
		Size: 33.1 MB (33061276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c151290e103ea7259c94eabc14a4eb58f0940c59479b1a74294dbaa1afefe6`  
		Last Modified: Tue, 16 Jan 2024 18:40:18 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.2-20-alpine3.19`

```console
$ docker pull mongo-express@sha256:65f053960cdc0b512ca9b0ca38ac66ddf79da9e17a55e0bb6f67ee429b87aca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.2-20-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:f073fe32e107c98acd895b93b5021b98c22fc5073eae662c5b123b80947415ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81764461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a98c1a3f58478f695597e44f0cdb4f09f8561a93ad6df3181949e73cd19b53`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 22:20:56 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 22:21:04 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 22:21:05 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 22:21:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 22:21:10 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 22:21:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 22:21:10 GMT
CMD ["node"]
# Wed, 10 Jan 2024 22:45:50 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 22:45:50 GMT
WORKDIR /app
# Wed, 10 Jan 2024 22:45:50 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 22:45:50 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 22:46:28 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:27 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:27 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:27 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:27 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:27 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be93293fd5362dfcc94826d8bd1f36150cb06ed2ed085d21d9dba20195faded7`  
		Last Modified: Wed, 10 Jan 2024 22:26:57 GMT  
		Size: 42.2 MB (42167339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376f9b7a67706b1a26941e182521e904295efb7b090d524a191417621d70d0db`  
		Last Modified: Wed, 10 Jan 2024 22:26:51 GMT  
		Size: 2.3 MB (2340977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e53c60b2bbe88730ffe3d177c7169bd98e824643e5f9fa3f2656e67725b35f5`  
		Last Modified: Wed, 10 Jan 2024 22:26:51 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ddba759d2d86f589c939f166c9e7785bfde0ad13339103a2baf045b8c65f82e`  
		Last Modified: Wed, 10 Jan 2024 22:47:44 GMT  
		Size: 784.7 KB (784693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a948b8e0cfe41ee16ce54ad2379081adab071f8072a1c88b0bb4e5d583a2488`  
		Last Modified: Wed, 10 Jan 2024 22:47:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dfe75b5784c4893073cb269ad92e672f447fffe9665a7806f5eef05182fcc3`  
		Last Modified: Wed, 10 Jan 2024 22:47:52 GMT  
		Size: 33.1 MB (33061544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df36fcf5d731bf74001ef6bbf1938576595ca763950a95dae8ff8293bd8e131`  
		Last Modified: Tue, 16 Jan 2024 18:33:54 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.2-20-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:1d8bdc2c5611867de62b9065ea15a8971ab63b4340a3902e24370f1fa6bbd6d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81624064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6e148ac6000b03eecc31b870a3940cbe6f080daf808742b028ccc2c0fac042`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 23:04:26 GMT
ENV NODE_VERSION=20.11.0
# Wed, 10 Jan 2024 23:27:39 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a8bec39586538896715be7a2ca7ef08727a58ad94d25876c5db11cafacff4c37" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Wed, 10 Jan 2024 23:27:39 GMT
ENV YARN_VERSION=1.22.19
# Wed, 10 Jan 2024 23:27:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Wed, 10 Jan 2024 23:27:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 10 Jan 2024 23:27:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 23:27:45 GMT
CMD ["node"]
# Wed, 10 Jan 2024 23:51:22 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Wed, 10 Jan 2024 23:51:22 GMT
WORKDIR /app
# Wed, 10 Jan 2024 23:51:22 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Wed, 10 Jan 2024 23:51:22 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Wed, 10 Jan 2024 23:51:57 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:44 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:44 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:44 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:44 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:44 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec53874fe288a72a8b7207e1695ec626ea0bc80a7c3fa3e872c694d1605add7`  
		Last Modified: Wed, 10 Jan 2024 23:33:12 GMT  
		Size: 42.0 MB (42010031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3946ff1ba9858829b3ccbb2f4b3e06515829d3847659ea96287591a76801fe29`  
		Last Modified: Wed, 10 Jan 2024 23:33:08 GMT  
		Size: 2.3 MB (2341097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2987d39b19e8c4f23a1841693e2ea0b850c3817af22d9a0623b2c9c351ef8b`  
		Last Modified: Wed, 10 Jan 2024 23:33:07 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75da99a625c30c70eb981856dd368a287a882717ea69362ccca1b67e03df34e1`  
		Last Modified: Wed, 10 Jan 2024 23:52:56 GMT  
		Size: 862.4 KB (862430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5b244dd2e8846301eca1dcfe6c573ddb6fccf80eef605bbf1712ada2a3e94e`  
		Last Modified: Wed, 10 Jan 2024 23:52:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7e8f1e56d4230365fce75aaf2cd1434d33278b700dac9419a17918437c4b93`  
		Last Modified: Wed, 10 Jan 2024 23:53:02 GMT  
		Size: 33.1 MB (33061288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dc3b5f41472b90f22cb37f290027e2e2588f82d5fdbcdc51dc1b9b5ad2a4bc`  
		Last Modified: Tue, 16 Jan 2024 18:40:08 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:latest`

```console
$ docker pull mongo-express@sha256:98ad29b0d7cbeeba8f4640cdcd11e097081ed0ca27c89b4ee0cde63e3bfe53f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:latest` - linux; amd64

```console
$ docker pull mongo-express@sha256:0cba5f35c950762b9093da01ae48c19e3088093eeef8cb119529fb298685552d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79724504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d527c213d73e59c6dcc7e8b090002a1f81503a790d78d47b34df8586ce8c252f`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 01:26:35 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 01:26:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 01:26:44 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 01:26:48 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 01:26:48 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 01:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 01:26:48 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:16:13 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:16:13 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:16:14 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:16:52 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:33:37 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:33:37 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:33:37 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:33:37 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:33:37 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7465dc4da3894941da9beb13e53fea672b4167e0031a049feea4cd6ed2cd79`  
		Last Modified: Sat, 02 Dec 2023 01:34:45 GMT  
		Size: 40.1 MB (40112458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7b2bf3cf64fb3d50ff099853b0df6438ea6163f4d9d2a7880856bd36a59ba2`  
		Last Modified: Sat, 02 Dec 2023 01:34:40 GMT  
		Size: 2.3 MB (2342890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3604fe7c8f3c53b8058f060dce2cfe269aad37881cabc3fa7b88c926470e9488`  
		Last Modified: Sat, 02 Dec 2023 01:34:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef732f87d67b9f901f90ed568ca4b4cea78c7d2a37219f3a6e76d7cc2d7a75cd`  
		Last Modified: Sat, 06 Jan 2024 01:18:28 GMT  
		Size: 802.3 KB (802311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2ade8248554eb9e4592da34eccdc1e3b1097a8d22046f414f26b3ebf05d2b0`  
		Last Modified: Sat, 06 Jan 2024 01:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bb6e5f1580826a520151543dc3f7e3e536b326b7aa1e21ef81ce4480e08f4c`  
		Last Modified: Sat, 06 Jan 2024 01:18:36 GMT  
		Size: 33.1 MB (33062997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b209d7438a256fbd0fdaf2e7fb7d233773023b8019b2928737937d51026977`  
		Last Modified: Tue, 16 Jan 2024 18:34:34 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:latest` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:a6846e70e124e9567bf389cf03d48b675f936ced5e4c0b65870cbe7062318a3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79444186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b30b6db7b34865b6126fd73f277de5fb3c193570fd3243921d7da8d63554c9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Sat, 02 Dec 2023 03:48:51 GMT
ENV NODE_VERSION=18.19.0
# Sat, 02 Dec 2023 04:09:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="10b7b23b6b867a25f060a433b83f5c3ecb3bcf7cdba1c0ce46443065a832fd41" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 02 Dec 2023 04:09:30 GMT
ENV YARN_VERSION=1.22.19
# Sat, 02 Dec 2023 04:09:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 02 Dec 2023 04:09:35 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 02 Dec 2023 04:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 04:09:35 GMT
CMD ["node"]
# Sat, 06 Jan 2024 01:56:27 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 06 Jan 2024 01:56:27 GMT
WORKDIR /app
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 06 Jan 2024 01:56:27 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 06 Jan 2024 01:56:59 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Tue, 16 Jan 2024 18:39:50 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Tue, 16 Jan 2024 18:39:50 GMT
EXPOSE 8081
# Tue, 16 Jan 2024 18:39:50 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Tue, 16 Jan 2024 18:39:50 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:50 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9cba98305bbc9b5b1acc82808c97ec2f1bdd0918782e26a4f249c89e8f5f1c`  
		Last Modified: Sat, 02 Dec 2023 04:17:12 GMT  
		Size: 39.8 MB (39817628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb1cdcfb3b6e7d1dbbdde57709e15e2c4bbdcac8f7c3da88459d74bc402c637`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 2.3 MB (2342686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266cff88a90930625e27a71f05f05b0bb69c1c3612e447e70131636367599c6c`  
		Last Modified: Sat, 02 Dec 2023 04:17:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b233574749281abc1a8ad5a8fb4f54bd3aa2b79c58bd876195c947c20d3083fa`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 887.0 KB (886996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1254cb9a9f437dc36f890b22f67330bfbc4c76a86d4e1c845d093039c3455c1e`  
		Last Modified: Sat, 06 Jan 2024 01:58:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca088f0889c67078200ebc911786a79a006f465a4c1e1a6fe630152a483e40bb`  
		Last Modified: Sat, 06 Jan 2024 01:58:29 GMT  
		Size: 33.1 MB (33062417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38362c10b0ee09dc1483616bb584925ef66302ceff20e0096c75f82025ca5fe`  
		Last Modified: Tue, 16 Jan 2024 18:40:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

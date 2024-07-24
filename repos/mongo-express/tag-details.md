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
$ docker pull mongo-express@sha256:1b23d7976f0210dbec74045c209e52fbb26d29b2e873d6c6fa3d3f0ae32c2a64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1` - linux; amd64

```console
$ docker pull mongo-express@sha256:16ec1773958dcc4baa97c9256ef36cb537f6fa86343f4d8b2eb65e174bdd13c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58932530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870141b735e7d896bde590765c341cdc64fb6d3284b5f6a81f70ec936e4d0b83`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a007eb24b0933d3275c67be086dc77622f1ff9832cd958c1e95c151f1a8a5`  
		Last Modified: Tue, 21 May 2024 17:38:21 GMT  
		Size: 39.7 MB (39701778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5189255e31c875046be6a3ece5ca5f1a54e136a8c8cba93e4e1bd790a5abe895`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 1.4 MB (1382340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4f8a6bc8d94f7f9fc9369452ba43b1da76575ce6afb0c273625b964aa59b2`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8305ae32c9545d17c51422ec6988c967b85c2ee1325fa52a21d4262dc00b2f8`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 802.3 KB (802260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b24ec126f9adddbf26755ef3d6e6018db3130be0a4351dc633de2be6f060a6`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7f59574f7db0afb123e92393fd591943720ba8325e2a93968ac03207463da9`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 13.6 MB (13642215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf3571b6cd74d1ca8d070d1eb0094fc337ca653706461fb355e6dc926087149`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1` - unknown; unknown

```console
$ docker pull mongo-express@sha256:413b1ec7d1063aa5d4c956b0c6a2bd41f2842c9e4bed60f2cf3630a300e7d419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.7 KB (871725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d93d63e9f733ec2ba4bdc53527eaeaaaacfb672032150579facdb0b05465ed`

```dockerfile
```

-	Layers:
	-	`sha256:99ef4db52d2b92160459751d6e67f7e46f3c8290ebdf5690ece278383f611ed5`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 853.8 KB (853771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337574bd0f5e62ff1a58c6c8e56823bd13fee68999327c2033bbd046d12788ef`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 18.0 KB (17954 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:366ed2adfdff5a80a5ba4dc2cda1292e11dd573d56c95b23fd7527d0abd57e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58604475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1133e12468c7959d2d714dc1278b56a843d9a62239ebee8cec8ae38b74443137`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c65f6bdf4051cd9c6f061b0cfda47467e3e58b16f74111cfd422f71de36f2f`  
		Last Modified: Tue, 21 May 2024 18:57:15 GMT  
		Size: 39.4 MB (39358407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ee6393f192419546b9f3e7c2a1dbf1e0cbb9ce899e97047710f672faa393c0`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 1.4 MB (1382328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5ec9da9bc085a79e5149ae99c65b3a4529a919d2d461bf77c6470176657763`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f541ec1a406728e856fa42c9c07bc7ec105c26f480f421bc5798b4a80970c82b`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 886.9 KB (886907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a17d49bb7c9b1c155f629f8aafbf911967fb0c524217fde3e1265650e2883d6`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa624262f6c2c0374cdf88f907432420ea08c1853c5080bd2a94732fcacbafb`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 13.6 MB (13642080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d515a8401de5b09984be00337670c33c2b0f1531b44941b1252a112aac3943`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1` - unknown; unknown

```console
$ docker pull mongo-express@sha256:1655dca624bd69180fb3a1517213cf766615e6f09654f909af74c562e61df657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.8 KB (871770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1e80e7198b9208ccc52fb3785bddaf5b948e1a3a3bc5dd6c8e998a9443bfc5`

```dockerfile
```

-	Layers:
	-	`sha256:0b5697ffa03ecd3e2d95c8f764886160a2f93212c0c552e5367c4930e7fe348e`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 853.8 KB (853794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14823bc6c9262151451390e9542239a27c7fc35b8b784ef2167081a33461b4ed`  
		Last Modified: Wed, 22 May 2024 01:27:36 GMT  
		Size: 18.0 KB (17976 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1-18`

```console
$ docker pull mongo-express@sha256:1b23d7976f0210dbec74045c209e52fbb26d29b2e873d6c6fa3d3f0ae32c2a64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1-18` - linux; amd64

```console
$ docker pull mongo-express@sha256:16ec1773958dcc4baa97c9256ef36cb537f6fa86343f4d8b2eb65e174bdd13c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58932530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870141b735e7d896bde590765c341cdc64fb6d3284b5f6a81f70ec936e4d0b83`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a007eb24b0933d3275c67be086dc77622f1ff9832cd958c1e95c151f1a8a5`  
		Last Modified: Tue, 21 May 2024 17:38:21 GMT  
		Size: 39.7 MB (39701778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5189255e31c875046be6a3ece5ca5f1a54e136a8c8cba93e4e1bd790a5abe895`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 1.4 MB (1382340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4f8a6bc8d94f7f9fc9369452ba43b1da76575ce6afb0c273625b964aa59b2`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8305ae32c9545d17c51422ec6988c967b85c2ee1325fa52a21d4262dc00b2f8`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 802.3 KB (802260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b24ec126f9adddbf26755ef3d6e6018db3130be0a4351dc633de2be6f060a6`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7f59574f7db0afb123e92393fd591943720ba8325e2a93968ac03207463da9`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 13.6 MB (13642215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf3571b6cd74d1ca8d070d1eb0094fc337ca653706461fb355e6dc926087149`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:413b1ec7d1063aa5d4c956b0c6a2bd41f2842c9e4bed60f2cf3630a300e7d419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.7 KB (871725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d93d63e9f733ec2ba4bdc53527eaeaaaacfb672032150579facdb0b05465ed`

```dockerfile
```

-	Layers:
	-	`sha256:99ef4db52d2b92160459751d6e67f7e46f3c8290ebdf5690ece278383f611ed5`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 853.8 KB (853771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337574bd0f5e62ff1a58c6c8e56823bd13fee68999327c2033bbd046d12788ef`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 18.0 KB (17954 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1-18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:366ed2adfdff5a80a5ba4dc2cda1292e11dd573d56c95b23fd7527d0abd57e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58604475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1133e12468c7959d2d714dc1278b56a843d9a62239ebee8cec8ae38b74443137`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c65f6bdf4051cd9c6f061b0cfda47467e3e58b16f74111cfd422f71de36f2f`  
		Last Modified: Tue, 21 May 2024 18:57:15 GMT  
		Size: 39.4 MB (39358407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ee6393f192419546b9f3e7c2a1dbf1e0cbb9ce899e97047710f672faa393c0`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 1.4 MB (1382328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5ec9da9bc085a79e5149ae99c65b3a4529a919d2d461bf77c6470176657763`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f541ec1a406728e856fa42c9c07bc7ec105c26f480f421bc5798b4a80970c82b`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 886.9 KB (886907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a17d49bb7c9b1c155f629f8aafbf911967fb0c524217fde3e1265650e2883d6`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa624262f6c2c0374cdf88f907432420ea08c1853c5080bd2a94732fcacbafb`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 13.6 MB (13642080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d515a8401de5b09984be00337670c33c2b0f1531b44941b1252a112aac3943`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:1655dca624bd69180fb3a1517213cf766615e6f09654f909af74c562e61df657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.8 KB (871770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1e80e7198b9208ccc52fb3785bddaf5b948e1a3a3bc5dd6c8e998a9443bfc5`

```dockerfile
```

-	Layers:
	-	`sha256:0b5697ffa03ecd3e2d95c8f764886160a2f93212c0c552e5367c4930e7fe348e`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 853.8 KB (853794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14823bc6c9262151451390e9542239a27c7fc35b8b784ef2167081a33461b4ed`  
		Last Modified: Wed, 22 May 2024 01:27:36 GMT  
		Size: 18.0 KB (17976 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1-18-alpine3.18`

```console
$ docker pull mongo-express@sha256:1b23d7976f0210dbec74045c209e52fbb26d29b2e873d6c6fa3d3f0ae32c2a64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1-18-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:16ec1773958dcc4baa97c9256ef36cb537f6fa86343f4d8b2eb65e174bdd13c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58932530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870141b735e7d896bde590765c341cdc64fb6d3284b5f6a81f70ec936e4d0b83`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a007eb24b0933d3275c67be086dc77622f1ff9832cd958c1e95c151f1a8a5`  
		Last Modified: Tue, 21 May 2024 17:38:21 GMT  
		Size: 39.7 MB (39701778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5189255e31c875046be6a3ece5ca5f1a54e136a8c8cba93e4e1bd790a5abe895`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 1.4 MB (1382340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4f8a6bc8d94f7f9fc9369452ba43b1da76575ce6afb0c273625b964aa59b2`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8305ae32c9545d17c51422ec6988c967b85c2ee1325fa52a21d4262dc00b2f8`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 802.3 KB (802260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b24ec126f9adddbf26755ef3d6e6018db3130be0a4351dc633de2be6f060a6`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7f59574f7db0afb123e92393fd591943720ba8325e2a93968ac03207463da9`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 13.6 MB (13642215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf3571b6cd74d1ca8d070d1eb0094fc337ca653706461fb355e6dc926087149`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-18-alpine3.18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:413b1ec7d1063aa5d4c956b0c6a2bd41f2842c9e4bed60f2cf3630a300e7d419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.7 KB (871725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d93d63e9f733ec2ba4bdc53527eaeaaaacfb672032150579facdb0b05465ed`

```dockerfile
```

-	Layers:
	-	`sha256:99ef4db52d2b92160459751d6e67f7e46f3c8290ebdf5690ece278383f611ed5`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 853.8 KB (853771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337574bd0f5e62ff1a58c6c8e56823bd13fee68999327c2033bbd046d12788ef`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 18.0 KB (17954 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1-18-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:366ed2adfdff5a80a5ba4dc2cda1292e11dd573d56c95b23fd7527d0abd57e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58604475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1133e12468c7959d2d714dc1278b56a843d9a62239ebee8cec8ae38b74443137`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c65f6bdf4051cd9c6f061b0cfda47467e3e58b16f74111cfd422f71de36f2f`  
		Last Modified: Tue, 21 May 2024 18:57:15 GMT  
		Size: 39.4 MB (39358407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ee6393f192419546b9f3e7c2a1dbf1e0cbb9ce899e97047710f672faa393c0`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 1.4 MB (1382328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5ec9da9bc085a79e5149ae99c65b3a4529a919d2d461bf77c6470176657763`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f541ec1a406728e856fa42c9c07bc7ec105c26f480f421bc5798b4a80970c82b`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 886.9 KB (886907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a17d49bb7c9b1c155f629f8aafbf911967fb0c524217fde3e1265650e2883d6`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa624262f6c2c0374cdf88f907432420ea08c1853c5080bd2a94732fcacbafb`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 13.6 MB (13642080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d515a8401de5b09984be00337670c33c2b0f1531b44941b1252a112aac3943`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-18-alpine3.18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:1655dca624bd69180fb3a1517213cf766615e6f09654f909af74c562e61df657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.8 KB (871770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1e80e7198b9208ccc52fb3785bddaf5b948e1a3a3bc5dd6c8e998a9443bfc5`

```dockerfile
```

-	Layers:
	-	`sha256:0b5697ffa03ecd3e2d95c8f764886160a2f93212c0c552e5367c4930e7fe348e`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 853.8 KB (853794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14823bc6c9262151451390e9542239a27c7fc35b8b784ef2167081a33461b4ed`  
		Last Modified: Wed, 22 May 2024 01:27:36 GMT  
		Size: 18.0 KB (17976 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1-18-alpine3.19`

```console
$ docker pull mongo-express@sha256:f2cb0f0ba1ce096c7401cfdccd025c4bc0684491cb0525e71546a6885486d32d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1-18-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:d5c18b7bf513dfa964190c6426cb5e1efc29b7202e71d0a7391fdc8dc94475a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59061137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342f2aca699c73e5f47e2c31368b0f49e959b6eef7ae6dfa74b3796bab26995a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.4
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
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
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bfd1a7f5d0b2ad6106b6097bf76f56d3a8c3bcc5cf7fa1f5d0a0ca9dc32cbc`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 39.8 MB (39831284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f16a148263d04e03d25d24411a9a48c71d7e31131900f4110b45b53c5a23ec`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 1.4 MB (1382231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30aa900b096c1999e57347eefc256ac6d0f228a2427efa4b8d9b2ec9152e74`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169da638993ed85f93c9e80244f3c282973a5d0ec0ecbb326127de99bf259310`  
		Last Modified: Tue, 23 Jul 2024 00:09:11 GMT  
		Size: 784.6 KB (784639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183fe892943f23a74e750a64320c615f2a2746c5b846b9af2b5fab8bd95d20d3`  
		Last Modified: Tue, 23 Jul 2024 00:09:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a85f23501d9ddab32f11f2c379b60ed3a2e68da4d6274d6eb71d2776d62912`  
		Last Modified: Tue, 23 Jul 2024 00:09:12 GMT  
		Size: 13.6 MB (13642551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9a502d228384829f99ad2dbcbcb0a8067c0428d7f3d9d2ddf81965f8fa66f9`  
		Last Modified: Tue, 23 Jul 2024 00:09:11 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-18-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:c4516269454877faf8c9692692b8a5496db8224ce01447ff300a5785f5dd19c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **952.4 KB (952382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07b786262bf0f0ba037b7e4a3b30acb1d842c6a1721c00598ca85c4ca15e166`

```dockerfile
```

-	Layers:
	-	`sha256:1687d253fb1176af9a484de43a19f21d7b95f56a9ef8e7ba2e65f26adcfd21a2`  
		Last Modified: Tue, 23 Jul 2024 00:09:11 GMT  
		Size: 937.1 KB (937118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcaf346464aea6b9ddb151968a41923bdb5e2e1a01b7fd4ce21d51a54db0fa7d`  
		Last Modified: Tue, 23 Jul 2024 00:09:11 GMT  
		Size: 15.3 KB (15264 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1-18-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:1917bfbd072111e6787c0d7671b70db1c48b5dedc8575d59980480a8668f0f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58784798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e9ea620d2df5f8d1ff60dbd50179071636ea950a054fcd17ec74c1a4443b9c`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.4
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
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
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d34fa575f3bac771ddb2aa598addd06eb8ee9021b249cbc0e60e5e9cd74885c`  
		Last Modified: Tue, 23 Jul 2024 21:29:17 GMT  
		Size: 39.5 MB (39537820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8ada097bad821da4edbdb4753ce1e3ca5ddf992a4bac4a2f723b4819ac2d96`  
		Last Modified: Tue, 23 Jul 2024 21:29:17 GMT  
		Size: 1.4 MB (1382238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae55db9b5c5d4ef1702f1307c5604009843d2a03b7e3b4d1e671c0d3c95abf7`  
		Last Modified: Tue, 23 Jul 2024 21:29:16 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3898847d95ac7116957cf14cf5dd521d07bf1b44db7d55981c543164bf297c69`  
		Last Modified: Wed, 24 Jul 2024 16:00:15 GMT  
		Size: 862.4 KB (862434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c176ed9423f7e5dd1d530f4a6d1b9a60e9b5569566c45d7e65ca4dc5f07c64d`  
		Last Modified: Wed, 24 Jul 2024 16:00:14 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a231052b9eefc4c140d03c6d5f3cf634b9bb0fa38dfe501968843a6ff5ed59`  
		Last Modified: Wed, 24 Jul 2024 16:00:15 GMT  
		Size: 13.6 MB (13642459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce42b3807b6cc5b97526394a23af24e77bb35e19cc16b9dc3009bfe62b025b51`  
		Last Modified: Wed, 24 Jul 2024 16:00:14 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-18-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:c827c59edcc29da428f7166481dd93ab56fb1c6467af525653473bf857c2067a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **952.8 KB (952829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e072a88d682d05035a2450fbe7c4ce1db321ac4083f9e0bdb19faf34f3e9d16`

```dockerfile
```

-	Layers:
	-	`sha256:9acdc47665608bbd190c9f2027affe013283907502482a7ace623d6dd3642cfb`  
		Last Modified: Wed, 24 Jul 2024 16:00:15 GMT  
		Size: 937.2 KB (937162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51a2bf33c3415b297374606c92d9214c5a62aafe68b47aa52e90e8ef3844b1b2`  
		Last Modified: Wed, 24 Jul 2024 16:00:14 GMT  
		Size: 15.7 KB (15667 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1-20`

```console
$ docker pull mongo-express@sha256:30fc6333779340217c6a2bc0bc3cd53aa46028ab8fc6caef41bd00bf0faacf53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1-20` - linux; amd64

```console
$ docker pull mongo-express@sha256:4efb9d899e2df08c2376e34d56d9540a8df8b6a77eb6494f7b99be2d33b7fa6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61319803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6389604d11ffa3b080a5dc390ee48f080dc3d6ba840f4ee700d55db6026460d`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.13.1
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a723c5566edc88aa2d53704f40a8be5984a6bb1eeac2d952577c8a13b6aacb7b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f45eb22fa20b605d639b56c941eee09d35f22e3308138f9ca549682f1ca3709`  
		Last Modified: Thu, 09 May 2024 19:33:09 GMT  
		Size: 42.1 MB (42090948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c695c2a88c4c3a8f44d4dcbbe13fe8035850eed2d96d550d162ac2494ce1057`  
		Last Modified: Thu, 09 May 2024 19:33:03 GMT  
		Size: 1.4 MB (1382339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb35f839ffe35efef3413fa7d570e3b7f760e058e0ce4e2d559a6cfeef49ed2d`  
		Last Modified: Thu, 09 May 2024 19:33:03 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6760b677c65af4266d44d87a523b05b4a46fd1f2cd629d823e2b32d87736e5c`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 802.3 KB (802254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d870e531048239a7f00267838e7b7aa1a6521b1327ba9af44f2e183933cc3bc9`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0923af95f273ca96c5940f7fdb8dd894937675f7356c2f3d0c070ad64f3383`  
		Last Modified: Thu, 16 May 2024 21:17:41 GMT  
		Size: 13.6 MB (13640323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d591368a3ca459ae6b7ff4033bf6ecca1ca6b106cf4c873f7ffb6cf63b37956e`  
		Last Modified: Thu, 16 May 2024 21:17:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-20` - unknown; unknown

```console
$ docker pull mongo-express@sha256:565f13d8fadcbc6339e7121f3a8bc22928659ff487338fb0fa9fcb71ec26aacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.2 KB (886250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75571567217624a0844467488c2ce51dc84aa41ac797431a3687bd519c6ed811`

```dockerfile
```

-	Layers:
	-	`sha256:384104d98c8c6327d8f0d8eafa856e2d67dc0afc729fed151aadef3d148e9766`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 869.5 KB (869526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428d1351fe0d5ab05317464cecc0248d9252bfbe39ad0bd36a3d2d2de94ac229`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 16.7 KB (16724 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1-20` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:61595f75f159e417270c976ca6ab7393ee3c734a930a7cc500b916ee1668d627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61086108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683f152e5af50adb0da95d01bdc58abfd463e14fcd33ac40445db458a937e855`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.13.1
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a723c5566edc88aa2d53704f40a8be5984a6bb1eeac2d952577c8a13b6aacb7b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79650a799acd01e8d1e1c75528816262c35bd29243bc36a6ef8c5fc119fbd452`  
		Last Modified: Thu, 09 May 2024 20:33:48 GMT  
		Size: 41.8 MB (41841782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2dc15869135031a1f26ac2fa8e6ead18a4ad8e4c5dcc08ffcf30b2e81d6f27`  
		Last Modified: Thu, 09 May 2024 20:33:44 GMT  
		Size: 1.4 MB (1382319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6bbcfe9ab8b72380fc1c1f4dabb2fb18dd5d1fb8c18f4c81e21a76dc563420`  
		Last Modified: Thu, 09 May 2024 20:33:43 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda9e6789178b6ca1e8f50340a02cc6ca3ea258c2b4e596333c45b130b891d9`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 886.9 KB (886915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81bf146f4e81f2aff2340a2041e79f94a81540c7d16a7c2becc72e4b780103f`  
		Last Modified: Thu, 16 May 2024 23:39:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacfc2ffce94d32dd6677e37c45532046c23dbb4b2183d51b9202aeb51a0b66`  
		Last Modified: Thu, 16 May 2024 23:39:28 GMT  
		Size: 13.6 MB (13640341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6391dab4f4159f0f7c4c965dc2b8155acb25f3f401394c7ae6479d7db60f8e`  
		Last Modified: Thu, 16 May 2024 23:39:28 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-20` - unknown; unknown

```console
$ docker pull mongo-express@sha256:726b54d4dbfbc3441cfed9dc5201370dd8ee05797523031f07fbedec5ab2262a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.3 KB (886277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c57ff4134182ff8945e2395e790022f7c6c2a6f043fb14dee74fd226b290ea`

```dockerfile
```

-	Layers:
	-	`sha256:a6a026c6678809f55212fb61571eff769609c21fb067cd587fe4d4f4006fe4fa`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 869.5 KB (869541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0c143a0a869c3080e8ae773c180060a4a88ec6940e736947d1cbec45d0c74b`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 16.7 KB (16736 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1-20-alpine3.18`

```console
$ docker pull mongo-express@sha256:30fc6333779340217c6a2bc0bc3cd53aa46028ab8fc6caef41bd00bf0faacf53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1-20-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:4efb9d899e2df08c2376e34d56d9540a8df8b6a77eb6494f7b99be2d33b7fa6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61319803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6389604d11ffa3b080a5dc390ee48f080dc3d6ba840f4ee700d55db6026460d`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.13.1
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a723c5566edc88aa2d53704f40a8be5984a6bb1eeac2d952577c8a13b6aacb7b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f45eb22fa20b605d639b56c941eee09d35f22e3308138f9ca549682f1ca3709`  
		Last Modified: Thu, 09 May 2024 19:33:09 GMT  
		Size: 42.1 MB (42090948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c695c2a88c4c3a8f44d4dcbbe13fe8035850eed2d96d550d162ac2494ce1057`  
		Last Modified: Thu, 09 May 2024 19:33:03 GMT  
		Size: 1.4 MB (1382339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb35f839ffe35efef3413fa7d570e3b7f760e058e0ce4e2d559a6cfeef49ed2d`  
		Last Modified: Thu, 09 May 2024 19:33:03 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6760b677c65af4266d44d87a523b05b4a46fd1f2cd629d823e2b32d87736e5c`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 802.3 KB (802254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d870e531048239a7f00267838e7b7aa1a6521b1327ba9af44f2e183933cc3bc9`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0923af95f273ca96c5940f7fdb8dd894937675f7356c2f3d0c070ad64f3383`  
		Last Modified: Thu, 16 May 2024 21:17:41 GMT  
		Size: 13.6 MB (13640323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d591368a3ca459ae6b7ff4033bf6ecca1ca6b106cf4c873f7ffb6cf63b37956e`  
		Last Modified: Thu, 16 May 2024 21:17:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-20-alpine3.18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:565f13d8fadcbc6339e7121f3a8bc22928659ff487338fb0fa9fcb71ec26aacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.2 KB (886250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75571567217624a0844467488c2ce51dc84aa41ac797431a3687bd519c6ed811`

```dockerfile
```

-	Layers:
	-	`sha256:384104d98c8c6327d8f0d8eafa856e2d67dc0afc729fed151aadef3d148e9766`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 869.5 KB (869526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428d1351fe0d5ab05317464cecc0248d9252bfbe39ad0bd36a3d2d2de94ac229`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 16.7 KB (16724 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1-20-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:61595f75f159e417270c976ca6ab7393ee3c734a930a7cc500b916ee1668d627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61086108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683f152e5af50adb0da95d01bdc58abfd463e14fcd33ac40445db458a937e855`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.13.1
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a723c5566edc88aa2d53704f40a8be5984a6bb1eeac2d952577c8a13b6aacb7b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79650a799acd01e8d1e1c75528816262c35bd29243bc36a6ef8c5fc119fbd452`  
		Last Modified: Thu, 09 May 2024 20:33:48 GMT  
		Size: 41.8 MB (41841782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2dc15869135031a1f26ac2fa8e6ead18a4ad8e4c5dcc08ffcf30b2e81d6f27`  
		Last Modified: Thu, 09 May 2024 20:33:44 GMT  
		Size: 1.4 MB (1382319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6bbcfe9ab8b72380fc1c1f4dabb2fb18dd5d1fb8c18f4c81e21a76dc563420`  
		Last Modified: Thu, 09 May 2024 20:33:43 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda9e6789178b6ca1e8f50340a02cc6ca3ea258c2b4e596333c45b130b891d9`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 886.9 KB (886915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81bf146f4e81f2aff2340a2041e79f94a81540c7d16a7c2becc72e4b780103f`  
		Last Modified: Thu, 16 May 2024 23:39:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacfc2ffce94d32dd6677e37c45532046c23dbb4b2183d51b9202aeb51a0b66`  
		Last Modified: Thu, 16 May 2024 23:39:28 GMT  
		Size: 13.6 MB (13640341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6391dab4f4159f0f7c4c965dc2b8155acb25f3f401394c7ae6479d7db60f8e`  
		Last Modified: Thu, 16 May 2024 23:39:28 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-20-alpine3.18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:726b54d4dbfbc3441cfed9dc5201370dd8ee05797523031f07fbedec5ab2262a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.3 KB (886277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c57ff4134182ff8945e2395e790022f7c6c2a6f043fb14dee74fd226b290ea`

```dockerfile
```

-	Layers:
	-	`sha256:a6a026c6678809f55212fb61571eff769609c21fb067cd587fe4d4f4006fe4fa`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 869.5 KB (869541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0c143a0a869c3080e8ae773c180060a4a88ec6940e736947d1cbec45d0c74b`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 16.7 KB (16736 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1-20-alpine3.19`

```console
$ docker pull mongo-express@sha256:b47630179d52a780c65cc547503d7953a4ac3f791eaa9d4e8f61243f6da54aa7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1-20-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:58a8b49f0c9abaf0f1ba430be1202e891d51402c2ab8383c733838fdccfead67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61478686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e136336c2760eeb853bcfd31f35924ca0d85d29aa1832396342fc1a4cb50528b`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.16.0
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="40efcec63e42ca58a39cc89c99d8852bd31ea09e046966b321fd337be999651d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
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
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec6334b9b0a790105fc39fe11022bb7c8b844a2c7e07b8bde337b7f4ff0c7df`  
		Last Modified: Wed, 24 Jul 2024 15:04:16 GMT  
		Size: 42.2 MB (42246294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8508bfb40de7bd1b0ef262a221277657f56967f8b948c757db72f7c4f4bddcf`  
		Last Modified: Wed, 24 Jul 2024 15:04:15 GMT  
		Size: 1.4 MB (1387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1368777c2a4047a6257f340e9d9b4d0a8e48ee04031b04f2754455a2348b9ada`  
		Last Modified: Wed, 24 Jul 2024 15:04:14 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0c462386bc3775c2812b964c489638c7f71254d3f3bbdcf51d2b902d0b2b1e`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 784.7 KB (784651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5e5b3c85d0bf7718ec6b944641d9ec27d34e69468d0d39ee74091e8b53c3b5`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be7b6ef8947ba420191f6792fcf34960cd81c6c61f3163999e36636cc928c42`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 13.6 MB (13640089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc9da1a3da68b8538b549b171acbb3b3aab0e2c0efcba0d6ee2c1060ef13c55`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-20-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:ab4548921cc928d8da7887ef88674cd70f5c5724d4b731fcb6b1efa7d0c41c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.9 KB (949881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1462946f370d02614aa083d2ac23608b6f88ce73e40ea9808a810400be4d605f`

```dockerfile
```

-	Layers:
	-	`sha256:b691f14cb639c942f583b3971e036f265d0ad849cdd0a2e4bd514af329a71238`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 934.6 KB (934617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f273552636b43c575cdcad65d7c6d95e419b9c49ba68507afb546ef44f218a`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 15.3 KB (15264 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1-20-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:66c693e57b78054d86a6088b1c2c8b4ddc9ba703cc7b66bcbbb9aa25728abc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61253372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66be16b21a747d26cb07888f6fce278e5b2a6a4aaa0034703555bee9d568e735`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.15.1
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a5263215500d0f53e4b5194791bb8753df2380977d603bf408f5bf897eaf0708" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
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
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8843ec14bb10ffc4526ea83f602e1539ee1ad3e50edf6b230548256d2e0471cd`  
		Last Modified: Tue, 09 Jul 2024 18:06:51 GMT  
		Size: 42.0 MB (42005159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1708aba65ae6b8151fc0769578a456a6dca12c3d591792ca4f27c1fc233d8b74`  
		Last Modified: Tue, 09 Jul 2024 18:06:50 GMT  
		Size: 1.4 MB (1387218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a34874eeafb2834712acef30c3588dad8614613833c11b0aadc655efb5fd97`  
		Last Modified: Tue, 09 Jul 2024 18:06:49 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc10fc459286d0eefdfd555f366630cb94bc79b8299ed733a71379b3452fb7cf`  
		Last Modified: Tue, 09 Jul 2024 20:45:55 GMT  
		Size: 862.4 KB (862417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70706fc6c11bffbe80832642bdf80f88aa3e1427565b60a67d437b8ac5a1481`  
		Last Modified: Tue, 09 Jul 2024 20:45:55 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1a508ca4ad871393390beb5747c5112652bbd561e5893c8dfd6af24f1e2309`  
		Last Modified: Tue, 09 Jul 2024 20:45:55 GMT  
		Size: 13.6 MB (13639987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f4238113fc86b109d16ffcd8abb04bbb6232158245846a112a1d37ca03bff5`  
		Last Modified: Tue, 09 Jul 2024 20:45:55 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-20-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:f05b4916fa918667d97f1e9aaa1999f3e250f30ba79ed2f6600850f4ac3347a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.8 KB (867802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f72482674dbc82edc9ccb33b3e10e6979a7dbf1f33156579b5584adc2e9df19`

```dockerfile
```

-	Layers:
	-	`sha256:0a0c792df95159c040e5177c7777e01688a678dacf8e9c0f8e0ace2ec5778dac`  
		Last Modified: Tue, 09 Jul 2024 20:45:54 GMT  
		Size: 852.1 KB (852135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e921a496e22ed15051735339925300b015e06a2a40df1a8c16c1111282cba06`  
		Last Modified: Tue, 09 Jul 2024 20:45:54 GMT  
		Size: 15.7 KB (15667 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1.0`

```console
$ docker pull mongo-express@sha256:1b23d7976f0210dbec74045c209e52fbb26d29b2e873d6c6fa3d3f0ae32c2a64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1.0` - linux; amd64

```console
$ docker pull mongo-express@sha256:16ec1773958dcc4baa97c9256ef36cb537f6fa86343f4d8b2eb65e174bdd13c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58932530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870141b735e7d896bde590765c341cdc64fb6d3284b5f6a81f70ec936e4d0b83`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a007eb24b0933d3275c67be086dc77622f1ff9832cd958c1e95c151f1a8a5`  
		Last Modified: Tue, 21 May 2024 17:38:21 GMT  
		Size: 39.7 MB (39701778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5189255e31c875046be6a3ece5ca5f1a54e136a8c8cba93e4e1bd790a5abe895`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 1.4 MB (1382340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4f8a6bc8d94f7f9fc9369452ba43b1da76575ce6afb0c273625b964aa59b2`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8305ae32c9545d17c51422ec6988c967b85c2ee1325fa52a21d4262dc00b2f8`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 802.3 KB (802260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b24ec126f9adddbf26755ef3d6e6018db3130be0a4351dc633de2be6f060a6`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7f59574f7db0afb123e92393fd591943720ba8325e2a93968ac03207463da9`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 13.6 MB (13642215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf3571b6cd74d1ca8d070d1eb0094fc337ca653706461fb355e6dc926087149`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0` - unknown; unknown

```console
$ docker pull mongo-express@sha256:413b1ec7d1063aa5d4c956b0c6a2bd41f2842c9e4bed60f2cf3630a300e7d419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.7 KB (871725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d93d63e9f733ec2ba4bdc53527eaeaaaacfb672032150579facdb0b05465ed`

```dockerfile
```

-	Layers:
	-	`sha256:99ef4db52d2b92160459751d6e67f7e46f3c8290ebdf5690ece278383f611ed5`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 853.8 KB (853771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337574bd0f5e62ff1a58c6c8e56823bd13fee68999327c2033bbd046d12788ef`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 18.0 KB (17954 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1.0` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:366ed2adfdff5a80a5ba4dc2cda1292e11dd573d56c95b23fd7527d0abd57e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58604475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1133e12468c7959d2d714dc1278b56a843d9a62239ebee8cec8ae38b74443137`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c65f6bdf4051cd9c6f061b0cfda47467e3e58b16f74111cfd422f71de36f2f`  
		Last Modified: Tue, 21 May 2024 18:57:15 GMT  
		Size: 39.4 MB (39358407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ee6393f192419546b9f3e7c2a1dbf1e0cbb9ce899e97047710f672faa393c0`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 1.4 MB (1382328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5ec9da9bc085a79e5149ae99c65b3a4529a919d2d461bf77c6470176657763`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f541ec1a406728e856fa42c9c07bc7ec105c26f480f421bc5798b4a80970c82b`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 886.9 KB (886907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a17d49bb7c9b1c155f629f8aafbf911967fb0c524217fde3e1265650e2883d6`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa624262f6c2c0374cdf88f907432420ea08c1853c5080bd2a94732fcacbafb`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 13.6 MB (13642080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d515a8401de5b09984be00337670c33c2b0f1531b44941b1252a112aac3943`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0` - unknown; unknown

```console
$ docker pull mongo-express@sha256:1655dca624bd69180fb3a1517213cf766615e6f09654f909af74c562e61df657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.8 KB (871770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1e80e7198b9208ccc52fb3785bddaf5b948e1a3a3bc5dd6c8e998a9443bfc5`

```dockerfile
```

-	Layers:
	-	`sha256:0b5697ffa03ecd3e2d95c8f764886160a2f93212c0c552e5367c4930e7fe348e`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 853.8 KB (853794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14823bc6c9262151451390e9542239a27c7fc35b8b784ef2167081a33461b4ed`  
		Last Modified: Wed, 22 May 2024 01:27:36 GMT  
		Size: 18.0 KB (17976 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1.0-18`

```console
$ docker pull mongo-express@sha256:1b23d7976f0210dbec74045c209e52fbb26d29b2e873d6c6fa3d3f0ae32c2a64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1.0-18` - linux; amd64

```console
$ docker pull mongo-express@sha256:16ec1773958dcc4baa97c9256ef36cb537f6fa86343f4d8b2eb65e174bdd13c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58932530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870141b735e7d896bde590765c341cdc64fb6d3284b5f6a81f70ec936e4d0b83`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a007eb24b0933d3275c67be086dc77622f1ff9832cd958c1e95c151f1a8a5`  
		Last Modified: Tue, 21 May 2024 17:38:21 GMT  
		Size: 39.7 MB (39701778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5189255e31c875046be6a3ece5ca5f1a54e136a8c8cba93e4e1bd790a5abe895`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 1.4 MB (1382340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4f8a6bc8d94f7f9fc9369452ba43b1da76575ce6afb0c273625b964aa59b2`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8305ae32c9545d17c51422ec6988c967b85c2ee1325fa52a21d4262dc00b2f8`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 802.3 KB (802260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b24ec126f9adddbf26755ef3d6e6018db3130be0a4351dc633de2be6f060a6`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7f59574f7db0afb123e92393fd591943720ba8325e2a93968ac03207463da9`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 13.6 MB (13642215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf3571b6cd74d1ca8d070d1eb0094fc337ca653706461fb355e6dc926087149`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0-18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:413b1ec7d1063aa5d4c956b0c6a2bd41f2842c9e4bed60f2cf3630a300e7d419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.7 KB (871725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d93d63e9f733ec2ba4bdc53527eaeaaaacfb672032150579facdb0b05465ed`

```dockerfile
```

-	Layers:
	-	`sha256:99ef4db52d2b92160459751d6e67f7e46f3c8290ebdf5690ece278383f611ed5`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 853.8 KB (853771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337574bd0f5e62ff1a58c6c8e56823bd13fee68999327c2033bbd046d12788ef`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 18.0 KB (17954 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1.0-18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:366ed2adfdff5a80a5ba4dc2cda1292e11dd573d56c95b23fd7527d0abd57e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58604475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1133e12468c7959d2d714dc1278b56a843d9a62239ebee8cec8ae38b74443137`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c65f6bdf4051cd9c6f061b0cfda47467e3e58b16f74111cfd422f71de36f2f`  
		Last Modified: Tue, 21 May 2024 18:57:15 GMT  
		Size: 39.4 MB (39358407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ee6393f192419546b9f3e7c2a1dbf1e0cbb9ce899e97047710f672faa393c0`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 1.4 MB (1382328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5ec9da9bc085a79e5149ae99c65b3a4529a919d2d461bf77c6470176657763`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f541ec1a406728e856fa42c9c07bc7ec105c26f480f421bc5798b4a80970c82b`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 886.9 KB (886907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a17d49bb7c9b1c155f629f8aafbf911967fb0c524217fde3e1265650e2883d6`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa624262f6c2c0374cdf88f907432420ea08c1853c5080bd2a94732fcacbafb`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 13.6 MB (13642080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d515a8401de5b09984be00337670c33c2b0f1531b44941b1252a112aac3943`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0-18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:1655dca624bd69180fb3a1517213cf766615e6f09654f909af74c562e61df657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.8 KB (871770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1e80e7198b9208ccc52fb3785bddaf5b948e1a3a3bc5dd6c8e998a9443bfc5`

```dockerfile
```

-	Layers:
	-	`sha256:0b5697ffa03ecd3e2d95c8f764886160a2f93212c0c552e5367c4930e7fe348e`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 853.8 KB (853794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14823bc6c9262151451390e9542239a27c7fc35b8b784ef2167081a33461b4ed`  
		Last Modified: Wed, 22 May 2024 01:27:36 GMT  
		Size: 18.0 KB (17976 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1.0-18-alpine3.18`

```console
$ docker pull mongo-express@sha256:1b23d7976f0210dbec74045c209e52fbb26d29b2e873d6c6fa3d3f0ae32c2a64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1.0-18-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:16ec1773958dcc4baa97c9256ef36cb537f6fa86343f4d8b2eb65e174bdd13c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58932530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870141b735e7d896bde590765c341cdc64fb6d3284b5f6a81f70ec936e4d0b83`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a007eb24b0933d3275c67be086dc77622f1ff9832cd958c1e95c151f1a8a5`  
		Last Modified: Tue, 21 May 2024 17:38:21 GMT  
		Size: 39.7 MB (39701778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5189255e31c875046be6a3ece5ca5f1a54e136a8c8cba93e4e1bd790a5abe895`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 1.4 MB (1382340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4f8a6bc8d94f7f9fc9369452ba43b1da76575ce6afb0c273625b964aa59b2`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8305ae32c9545d17c51422ec6988c967b85c2ee1325fa52a21d4262dc00b2f8`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 802.3 KB (802260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b24ec126f9adddbf26755ef3d6e6018db3130be0a4351dc633de2be6f060a6`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7f59574f7db0afb123e92393fd591943720ba8325e2a93968ac03207463da9`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 13.6 MB (13642215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf3571b6cd74d1ca8d070d1eb0094fc337ca653706461fb355e6dc926087149`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0-18-alpine3.18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:413b1ec7d1063aa5d4c956b0c6a2bd41f2842c9e4bed60f2cf3630a300e7d419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.7 KB (871725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d93d63e9f733ec2ba4bdc53527eaeaaaacfb672032150579facdb0b05465ed`

```dockerfile
```

-	Layers:
	-	`sha256:99ef4db52d2b92160459751d6e67f7e46f3c8290ebdf5690ece278383f611ed5`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 853.8 KB (853771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337574bd0f5e62ff1a58c6c8e56823bd13fee68999327c2033bbd046d12788ef`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 18.0 KB (17954 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1.0-18-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:366ed2adfdff5a80a5ba4dc2cda1292e11dd573d56c95b23fd7527d0abd57e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58604475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1133e12468c7959d2d714dc1278b56a843d9a62239ebee8cec8ae38b74443137`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c65f6bdf4051cd9c6f061b0cfda47467e3e58b16f74111cfd422f71de36f2f`  
		Last Modified: Tue, 21 May 2024 18:57:15 GMT  
		Size: 39.4 MB (39358407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ee6393f192419546b9f3e7c2a1dbf1e0cbb9ce899e97047710f672faa393c0`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 1.4 MB (1382328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5ec9da9bc085a79e5149ae99c65b3a4529a919d2d461bf77c6470176657763`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f541ec1a406728e856fa42c9c07bc7ec105c26f480f421bc5798b4a80970c82b`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 886.9 KB (886907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a17d49bb7c9b1c155f629f8aafbf911967fb0c524217fde3e1265650e2883d6`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa624262f6c2c0374cdf88f907432420ea08c1853c5080bd2a94732fcacbafb`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 13.6 MB (13642080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d515a8401de5b09984be00337670c33c2b0f1531b44941b1252a112aac3943`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0-18-alpine3.18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:1655dca624bd69180fb3a1517213cf766615e6f09654f909af74c562e61df657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.8 KB (871770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1e80e7198b9208ccc52fb3785bddaf5b948e1a3a3bc5dd6c8e998a9443bfc5`

```dockerfile
```

-	Layers:
	-	`sha256:0b5697ffa03ecd3e2d95c8f764886160a2f93212c0c552e5367c4930e7fe348e`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 853.8 KB (853794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14823bc6c9262151451390e9542239a27c7fc35b8b784ef2167081a33461b4ed`  
		Last Modified: Wed, 22 May 2024 01:27:36 GMT  
		Size: 18.0 KB (17976 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1.0-18-alpine3.19`

```console
$ docker pull mongo-express@sha256:f2cb0f0ba1ce096c7401cfdccd025c4bc0684491cb0525e71546a6885486d32d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1.0-18-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:d5c18b7bf513dfa964190c6426cb5e1efc29b7202e71d0a7391fdc8dc94475a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59061137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342f2aca699c73e5f47e2c31368b0f49e959b6eef7ae6dfa74b3796bab26995a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.4
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
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
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bfd1a7f5d0b2ad6106b6097bf76f56d3a8c3bcc5cf7fa1f5d0a0ca9dc32cbc`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 39.8 MB (39831284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f16a148263d04e03d25d24411a9a48c71d7e31131900f4110b45b53c5a23ec`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 1.4 MB (1382231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30aa900b096c1999e57347eefc256ac6d0f228a2427efa4b8d9b2ec9152e74`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169da638993ed85f93c9e80244f3c282973a5d0ec0ecbb326127de99bf259310`  
		Last Modified: Tue, 23 Jul 2024 00:09:11 GMT  
		Size: 784.6 KB (784639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183fe892943f23a74e750a64320c615f2a2746c5b846b9af2b5fab8bd95d20d3`  
		Last Modified: Tue, 23 Jul 2024 00:09:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a85f23501d9ddab32f11f2c379b60ed3a2e68da4d6274d6eb71d2776d62912`  
		Last Modified: Tue, 23 Jul 2024 00:09:12 GMT  
		Size: 13.6 MB (13642551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9a502d228384829f99ad2dbcbcb0a8067c0428d7f3d9d2ddf81965f8fa66f9`  
		Last Modified: Tue, 23 Jul 2024 00:09:11 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0-18-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:c4516269454877faf8c9692692b8a5496db8224ce01447ff300a5785f5dd19c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **952.4 KB (952382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07b786262bf0f0ba037b7e4a3b30acb1d842c6a1721c00598ca85c4ca15e166`

```dockerfile
```

-	Layers:
	-	`sha256:1687d253fb1176af9a484de43a19f21d7b95f56a9ef8e7ba2e65f26adcfd21a2`  
		Last Modified: Tue, 23 Jul 2024 00:09:11 GMT  
		Size: 937.1 KB (937118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcaf346464aea6b9ddb151968a41923bdb5e2e1a01b7fd4ce21d51a54db0fa7d`  
		Last Modified: Tue, 23 Jul 2024 00:09:11 GMT  
		Size: 15.3 KB (15264 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1.0-18-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:1917bfbd072111e6787c0d7671b70db1c48b5dedc8575d59980480a8668f0f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58784798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e9ea620d2df5f8d1ff60dbd50179071636ea950a054fcd17ec74c1a4443b9c`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.4
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
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
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d34fa575f3bac771ddb2aa598addd06eb8ee9021b249cbc0e60e5e9cd74885c`  
		Last Modified: Tue, 23 Jul 2024 21:29:17 GMT  
		Size: 39.5 MB (39537820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8ada097bad821da4edbdb4753ce1e3ca5ddf992a4bac4a2f723b4819ac2d96`  
		Last Modified: Tue, 23 Jul 2024 21:29:17 GMT  
		Size: 1.4 MB (1382238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae55db9b5c5d4ef1702f1307c5604009843d2a03b7e3b4d1e671c0d3c95abf7`  
		Last Modified: Tue, 23 Jul 2024 21:29:16 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3898847d95ac7116957cf14cf5dd521d07bf1b44db7d55981c543164bf297c69`  
		Last Modified: Wed, 24 Jul 2024 16:00:15 GMT  
		Size: 862.4 KB (862434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c176ed9423f7e5dd1d530f4a6d1b9a60e9b5569566c45d7e65ca4dc5f07c64d`  
		Last Modified: Wed, 24 Jul 2024 16:00:14 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a231052b9eefc4c140d03c6d5f3cf634b9bb0fa38dfe501968843a6ff5ed59`  
		Last Modified: Wed, 24 Jul 2024 16:00:15 GMT  
		Size: 13.6 MB (13642459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce42b3807b6cc5b97526394a23af24e77bb35e19cc16b9dc3009bfe62b025b51`  
		Last Modified: Wed, 24 Jul 2024 16:00:14 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0-18-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:c827c59edcc29da428f7166481dd93ab56fb1c6467af525653473bf857c2067a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **952.8 KB (952829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e072a88d682d05035a2450fbe7c4ce1db321ac4083f9e0bdb19faf34f3e9d16`

```dockerfile
```

-	Layers:
	-	`sha256:9acdc47665608bbd190c9f2027affe013283907502482a7ace623d6dd3642cfb`  
		Last Modified: Wed, 24 Jul 2024 16:00:15 GMT  
		Size: 937.2 KB (937162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51a2bf33c3415b297374606c92d9214c5a62aafe68b47aa52e90e8ef3844b1b2`  
		Last Modified: Wed, 24 Jul 2024 16:00:14 GMT  
		Size: 15.7 KB (15667 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1.0-20`

```console
$ docker pull mongo-express@sha256:30fc6333779340217c6a2bc0bc3cd53aa46028ab8fc6caef41bd00bf0faacf53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1.0-20` - linux; amd64

```console
$ docker pull mongo-express@sha256:4efb9d899e2df08c2376e34d56d9540a8df8b6a77eb6494f7b99be2d33b7fa6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61319803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6389604d11ffa3b080a5dc390ee48f080dc3d6ba840f4ee700d55db6026460d`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.13.1
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a723c5566edc88aa2d53704f40a8be5984a6bb1eeac2d952577c8a13b6aacb7b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f45eb22fa20b605d639b56c941eee09d35f22e3308138f9ca549682f1ca3709`  
		Last Modified: Thu, 09 May 2024 19:33:09 GMT  
		Size: 42.1 MB (42090948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c695c2a88c4c3a8f44d4dcbbe13fe8035850eed2d96d550d162ac2494ce1057`  
		Last Modified: Thu, 09 May 2024 19:33:03 GMT  
		Size: 1.4 MB (1382339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb35f839ffe35efef3413fa7d570e3b7f760e058e0ce4e2d559a6cfeef49ed2d`  
		Last Modified: Thu, 09 May 2024 19:33:03 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6760b677c65af4266d44d87a523b05b4a46fd1f2cd629d823e2b32d87736e5c`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 802.3 KB (802254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d870e531048239a7f00267838e7b7aa1a6521b1327ba9af44f2e183933cc3bc9`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0923af95f273ca96c5940f7fdb8dd894937675f7356c2f3d0c070ad64f3383`  
		Last Modified: Thu, 16 May 2024 21:17:41 GMT  
		Size: 13.6 MB (13640323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d591368a3ca459ae6b7ff4033bf6ecca1ca6b106cf4c873f7ffb6cf63b37956e`  
		Last Modified: Thu, 16 May 2024 21:17:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0-20` - unknown; unknown

```console
$ docker pull mongo-express@sha256:565f13d8fadcbc6339e7121f3a8bc22928659ff487338fb0fa9fcb71ec26aacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.2 KB (886250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75571567217624a0844467488c2ce51dc84aa41ac797431a3687bd519c6ed811`

```dockerfile
```

-	Layers:
	-	`sha256:384104d98c8c6327d8f0d8eafa856e2d67dc0afc729fed151aadef3d148e9766`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 869.5 KB (869526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428d1351fe0d5ab05317464cecc0248d9252bfbe39ad0bd36a3d2d2de94ac229`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 16.7 KB (16724 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1.0-20` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:61595f75f159e417270c976ca6ab7393ee3c734a930a7cc500b916ee1668d627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61086108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683f152e5af50adb0da95d01bdc58abfd463e14fcd33ac40445db458a937e855`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.13.1
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a723c5566edc88aa2d53704f40a8be5984a6bb1eeac2d952577c8a13b6aacb7b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79650a799acd01e8d1e1c75528816262c35bd29243bc36a6ef8c5fc119fbd452`  
		Last Modified: Thu, 09 May 2024 20:33:48 GMT  
		Size: 41.8 MB (41841782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2dc15869135031a1f26ac2fa8e6ead18a4ad8e4c5dcc08ffcf30b2e81d6f27`  
		Last Modified: Thu, 09 May 2024 20:33:44 GMT  
		Size: 1.4 MB (1382319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6bbcfe9ab8b72380fc1c1f4dabb2fb18dd5d1fb8c18f4c81e21a76dc563420`  
		Last Modified: Thu, 09 May 2024 20:33:43 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda9e6789178b6ca1e8f50340a02cc6ca3ea258c2b4e596333c45b130b891d9`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 886.9 KB (886915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81bf146f4e81f2aff2340a2041e79f94a81540c7d16a7c2becc72e4b780103f`  
		Last Modified: Thu, 16 May 2024 23:39:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacfc2ffce94d32dd6677e37c45532046c23dbb4b2183d51b9202aeb51a0b66`  
		Last Modified: Thu, 16 May 2024 23:39:28 GMT  
		Size: 13.6 MB (13640341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6391dab4f4159f0f7c4c965dc2b8155acb25f3f401394c7ae6479d7db60f8e`  
		Last Modified: Thu, 16 May 2024 23:39:28 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0-20` - unknown; unknown

```console
$ docker pull mongo-express@sha256:726b54d4dbfbc3441cfed9dc5201370dd8ee05797523031f07fbedec5ab2262a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.3 KB (886277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c57ff4134182ff8945e2395e790022f7c6c2a6f043fb14dee74fd226b290ea`

```dockerfile
```

-	Layers:
	-	`sha256:a6a026c6678809f55212fb61571eff769609c21fb067cd587fe4d4f4006fe4fa`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 869.5 KB (869541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0c143a0a869c3080e8ae773c180060a4a88ec6940e736947d1cbec45d0c74b`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 16.7 KB (16736 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1.0-20-alpine3.18`

```console
$ docker pull mongo-express@sha256:30fc6333779340217c6a2bc0bc3cd53aa46028ab8fc6caef41bd00bf0faacf53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1.0-20-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:4efb9d899e2df08c2376e34d56d9540a8df8b6a77eb6494f7b99be2d33b7fa6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61319803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6389604d11ffa3b080a5dc390ee48f080dc3d6ba840f4ee700d55db6026460d`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.13.1
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a723c5566edc88aa2d53704f40a8be5984a6bb1eeac2d952577c8a13b6aacb7b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f45eb22fa20b605d639b56c941eee09d35f22e3308138f9ca549682f1ca3709`  
		Last Modified: Thu, 09 May 2024 19:33:09 GMT  
		Size: 42.1 MB (42090948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c695c2a88c4c3a8f44d4dcbbe13fe8035850eed2d96d550d162ac2494ce1057`  
		Last Modified: Thu, 09 May 2024 19:33:03 GMT  
		Size: 1.4 MB (1382339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb35f839ffe35efef3413fa7d570e3b7f760e058e0ce4e2d559a6cfeef49ed2d`  
		Last Modified: Thu, 09 May 2024 19:33:03 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6760b677c65af4266d44d87a523b05b4a46fd1f2cd629d823e2b32d87736e5c`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 802.3 KB (802254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d870e531048239a7f00267838e7b7aa1a6521b1327ba9af44f2e183933cc3bc9`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0923af95f273ca96c5940f7fdb8dd894937675f7356c2f3d0c070ad64f3383`  
		Last Modified: Thu, 16 May 2024 21:17:41 GMT  
		Size: 13.6 MB (13640323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d591368a3ca459ae6b7ff4033bf6ecca1ca6b106cf4c873f7ffb6cf63b37956e`  
		Last Modified: Thu, 16 May 2024 21:17:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0-20-alpine3.18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:565f13d8fadcbc6339e7121f3a8bc22928659ff487338fb0fa9fcb71ec26aacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.2 KB (886250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75571567217624a0844467488c2ce51dc84aa41ac797431a3687bd519c6ed811`

```dockerfile
```

-	Layers:
	-	`sha256:384104d98c8c6327d8f0d8eafa856e2d67dc0afc729fed151aadef3d148e9766`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 869.5 KB (869526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428d1351fe0d5ab05317464cecc0248d9252bfbe39ad0bd36a3d2d2de94ac229`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 16.7 KB (16724 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1.0-20-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:61595f75f159e417270c976ca6ab7393ee3c734a930a7cc500b916ee1668d627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61086108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683f152e5af50adb0da95d01bdc58abfd463e14fcd33ac40445db458a937e855`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.13.1
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a723c5566edc88aa2d53704f40a8be5984a6bb1eeac2d952577c8a13b6aacb7b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79650a799acd01e8d1e1c75528816262c35bd29243bc36a6ef8c5fc119fbd452`  
		Last Modified: Thu, 09 May 2024 20:33:48 GMT  
		Size: 41.8 MB (41841782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2dc15869135031a1f26ac2fa8e6ead18a4ad8e4c5dcc08ffcf30b2e81d6f27`  
		Last Modified: Thu, 09 May 2024 20:33:44 GMT  
		Size: 1.4 MB (1382319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6bbcfe9ab8b72380fc1c1f4dabb2fb18dd5d1fb8c18f4c81e21a76dc563420`  
		Last Modified: Thu, 09 May 2024 20:33:43 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda9e6789178b6ca1e8f50340a02cc6ca3ea258c2b4e596333c45b130b891d9`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 886.9 KB (886915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81bf146f4e81f2aff2340a2041e79f94a81540c7d16a7c2becc72e4b780103f`  
		Last Modified: Thu, 16 May 2024 23:39:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacfc2ffce94d32dd6677e37c45532046c23dbb4b2183d51b9202aeb51a0b66`  
		Last Modified: Thu, 16 May 2024 23:39:28 GMT  
		Size: 13.6 MB (13640341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6391dab4f4159f0f7c4c965dc2b8155acb25f3f401394c7ae6479d7db60f8e`  
		Last Modified: Thu, 16 May 2024 23:39:28 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0-20-alpine3.18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:726b54d4dbfbc3441cfed9dc5201370dd8ee05797523031f07fbedec5ab2262a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.3 KB (886277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c57ff4134182ff8945e2395e790022f7c6c2a6f043fb14dee74fd226b290ea`

```dockerfile
```

-	Layers:
	-	`sha256:a6a026c6678809f55212fb61571eff769609c21fb067cd587fe4d4f4006fe4fa`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 869.5 KB (869541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0c143a0a869c3080e8ae773c180060a4a88ec6940e736947d1cbec45d0c74b`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 16.7 KB (16736 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1.0-20-alpine3.19`

```console
$ docker pull mongo-express@sha256:b47630179d52a780c65cc547503d7953a4ac3f791eaa9d4e8f61243f6da54aa7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1.0-20-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:58a8b49f0c9abaf0f1ba430be1202e891d51402c2ab8383c733838fdccfead67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61478686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e136336c2760eeb853bcfd31f35924ca0d85d29aa1832396342fc1a4cb50528b`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.16.0
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="40efcec63e42ca58a39cc89c99d8852bd31ea09e046966b321fd337be999651d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
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
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec6334b9b0a790105fc39fe11022bb7c8b844a2c7e07b8bde337b7f4ff0c7df`  
		Last Modified: Wed, 24 Jul 2024 15:04:16 GMT  
		Size: 42.2 MB (42246294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8508bfb40de7bd1b0ef262a221277657f56967f8b948c757db72f7c4f4bddcf`  
		Last Modified: Wed, 24 Jul 2024 15:04:15 GMT  
		Size: 1.4 MB (1387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1368777c2a4047a6257f340e9d9b4d0a8e48ee04031b04f2754455a2348b9ada`  
		Last Modified: Wed, 24 Jul 2024 15:04:14 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0c462386bc3775c2812b964c489638c7f71254d3f3bbdcf51d2b902d0b2b1e`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 784.7 KB (784651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5e5b3c85d0bf7718ec6b944641d9ec27d34e69468d0d39ee74091e8b53c3b5`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be7b6ef8947ba420191f6792fcf34960cd81c6c61f3163999e36636cc928c42`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 13.6 MB (13640089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc9da1a3da68b8538b549b171acbb3b3aab0e2c0efcba0d6ee2c1060ef13c55`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0-20-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:ab4548921cc928d8da7887ef88674cd70f5c5724d4b731fcb6b1efa7d0c41c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.9 KB (949881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1462946f370d02614aa083d2ac23608b6f88ce73e40ea9808a810400be4d605f`

```dockerfile
```

-	Layers:
	-	`sha256:b691f14cb639c942f583b3971e036f265d0ad849cdd0a2e4bd514af329a71238`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 934.6 KB (934617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f273552636b43c575cdcad65d7c6d95e419b9c49ba68507afb546ef44f218a`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 15.3 KB (15264 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1.0-20-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:66c693e57b78054d86a6088b1c2c8b4ddc9ba703cc7b66bcbbb9aa25728abc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61253372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66be16b21a747d26cb07888f6fce278e5b2a6a4aaa0034703555bee9d568e735`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.15.1
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a5263215500d0f53e4b5194791bb8753df2380977d603bf408f5bf897eaf0708" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
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
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8843ec14bb10ffc4526ea83f602e1539ee1ad3e50edf6b230548256d2e0471cd`  
		Last Modified: Tue, 09 Jul 2024 18:06:51 GMT  
		Size: 42.0 MB (42005159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1708aba65ae6b8151fc0769578a456a6dca12c3d591792ca4f27c1fc233d8b74`  
		Last Modified: Tue, 09 Jul 2024 18:06:50 GMT  
		Size: 1.4 MB (1387218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a34874eeafb2834712acef30c3588dad8614613833c11b0aadc655efb5fd97`  
		Last Modified: Tue, 09 Jul 2024 18:06:49 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc10fc459286d0eefdfd555f366630cb94bc79b8299ed733a71379b3452fb7cf`  
		Last Modified: Tue, 09 Jul 2024 20:45:55 GMT  
		Size: 862.4 KB (862417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70706fc6c11bffbe80832642bdf80f88aa3e1427565b60a67d437b8ac5a1481`  
		Last Modified: Tue, 09 Jul 2024 20:45:55 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1a508ca4ad871393390beb5747c5112652bbd561e5893c8dfd6af24f1e2309`  
		Last Modified: Tue, 09 Jul 2024 20:45:55 GMT  
		Size: 13.6 MB (13639987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f4238113fc86b109d16ffcd8abb04bbb6232158245846a112a1d37ca03bff5`  
		Last Modified: Tue, 09 Jul 2024 20:45:55 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0-20-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:f05b4916fa918667d97f1e9aaa1999f3e250f30ba79ed2f6600850f4ac3347a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.8 KB (867802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f72482674dbc82edc9ccb33b3e10e6979a7dbf1f33156579b5584adc2e9df19`

```dockerfile
```

-	Layers:
	-	`sha256:0a0c792df95159c040e5177c7777e01688a678dacf8e9c0f8e0ace2ec5778dac`  
		Last Modified: Tue, 09 Jul 2024 20:45:54 GMT  
		Size: 852.1 KB (852135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e921a496e22ed15051735339925300b015e06a2a40df1a8c16c1111282cba06`  
		Last Modified: Tue, 09 Jul 2024 20:45:54 GMT  
		Size: 15.7 KB (15667 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1.0.2`

```console
$ docker pull mongo-express@sha256:1b23d7976f0210dbec74045c209e52fbb26d29b2e873d6c6fa3d3f0ae32c2a64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1.0.2` - linux; amd64

```console
$ docker pull mongo-express@sha256:16ec1773958dcc4baa97c9256ef36cb537f6fa86343f4d8b2eb65e174bdd13c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58932530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870141b735e7d896bde590765c341cdc64fb6d3284b5f6a81f70ec936e4d0b83`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a007eb24b0933d3275c67be086dc77622f1ff9832cd958c1e95c151f1a8a5`  
		Last Modified: Tue, 21 May 2024 17:38:21 GMT  
		Size: 39.7 MB (39701778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5189255e31c875046be6a3ece5ca5f1a54e136a8c8cba93e4e1bd790a5abe895`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 1.4 MB (1382340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4f8a6bc8d94f7f9fc9369452ba43b1da76575ce6afb0c273625b964aa59b2`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8305ae32c9545d17c51422ec6988c967b85c2ee1325fa52a21d4262dc00b2f8`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 802.3 KB (802260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b24ec126f9adddbf26755ef3d6e6018db3130be0a4351dc633de2be6f060a6`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7f59574f7db0afb123e92393fd591943720ba8325e2a93968ac03207463da9`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 13.6 MB (13642215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf3571b6cd74d1ca8d070d1eb0094fc337ca653706461fb355e6dc926087149`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0.2` - unknown; unknown

```console
$ docker pull mongo-express@sha256:413b1ec7d1063aa5d4c956b0c6a2bd41f2842c9e4bed60f2cf3630a300e7d419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.7 KB (871725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d93d63e9f733ec2ba4bdc53527eaeaaaacfb672032150579facdb0b05465ed`

```dockerfile
```

-	Layers:
	-	`sha256:99ef4db52d2b92160459751d6e67f7e46f3c8290ebdf5690ece278383f611ed5`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 853.8 KB (853771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337574bd0f5e62ff1a58c6c8e56823bd13fee68999327c2033bbd046d12788ef`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 18.0 KB (17954 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1.0.2` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:366ed2adfdff5a80a5ba4dc2cda1292e11dd573d56c95b23fd7527d0abd57e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58604475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1133e12468c7959d2d714dc1278b56a843d9a62239ebee8cec8ae38b74443137`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c65f6bdf4051cd9c6f061b0cfda47467e3e58b16f74111cfd422f71de36f2f`  
		Last Modified: Tue, 21 May 2024 18:57:15 GMT  
		Size: 39.4 MB (39358407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ee6393f192419546b9f3e7c2a1dbf1e0cbb9ce899e97047710f672faa393c0`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 1.4 MB (1382328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5ec9da9bc085a79e5149ae99c65b3a4529a919d2d461bf77c6470176657763`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f541ec1a406728e856fa42c9c07bc7ec105c26f480f421bc5798b4a80970c82b`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 886.9 KB (886907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a17d49bb7c9b1c155f629f8aafbf911967fb0c524217fde3e1265650e2883d6`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa624262f6c2c0374cdf88f907432420ea08c1853c5080bd2a94732fcacbafb`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 13.6 MB (13642080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d515a8401de5b09984be00337670c33c2b0f1531b44941b1252a112aac3943`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0.2` - unknown; unknown

```console
$ docker pull mongo-express@sha256:1655dca624bd69180fb3a1517213cf766615e6f09654f909af74c562e61df657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.8 KB (871770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1e80e7198b9208ccc52fb3785bddaf5b948e1a3a3bc5dd6c8e998a9443bfc5`

```dockerfile
```

-	Layers:
	-	`sha256:0b5697ffa03ecd3e2d95c8f764886160a2f93212c0c552e5367c4930e7fe348e`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 853.8 KB (853794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14823bc6c9262151451390e9542239a27c7fc35b8b784ef2167081a33461b4ed`  
		Last Modified: Wed, 22 May 2024 01:27:36 GMT  
		Size: 18.0 KB (17976 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1.0.2-18`

```console
$ docker pull mongo-express@sha256:1b23d7976f0210dbec74045c209e52fbb26d29b2e873d6c6fa3d3f0ae32c2a64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1.0.2-18` - linux; amd64

```console
$ docker pull mongo-express@sha256:16ec1773958dcc4baa97c9256ef36cb537f6fa86343f4d8b2eb65e174bdd13c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58932530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870141b735e7d896bde590765c341cdc64fb6d3284b5f6a81f70ec936e4d0b83`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a007eb24b0933d3275c67be086dc77622f1ff9832cd958c1e95c151f1a8a5`  
		Last Modified: Tue, 21 May 2024 17:38:21 GMT  
		Size: 39.7 MB (39701778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5189255e31c875046be6a3ece5ca5f1a54e136a8c8cba93e4e1bd790a5abe895`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 1.4 MB (1382340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4f8a6bc8d94f7f9fc9369452ba43b1da76575ce6afb0c273625b964aa59b2`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8305ae32c9545d17c51422ec6988c967b85c2ee1325fa52a21d4262dc00b2f8`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 802.3 KB (802260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b24ec126f9adddbf26755ef3d6e6018db3130be0a4351dc633de2be6f060a6`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7f59574f7db0afb123e92393fd591943720ba8325e2a93968ac03207463da9`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 13.6 MB (13642215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf3571b6cd74d1ca8d070d1eb0094fc337ca653706461fb355e6dc926087149`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0.2-18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:413b1ec7d1063aa5d4c956b0c6a2bd41f2842c9e4bed60f2cf3630a300e7d419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.7 KB (871725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d93d63e9f733ec2ba4bdc53527eaeaaaacfb672032150579facdb0b05465ed`

```dockerfile
```

-	Layers:
	-	`sha256:99ef4db52d2b92160459751d6e67f7e46f3c8290ebdf5690ece278383f611ed5`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 853.8 KB (853771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337574bd0f5e62ff1a58c6c8e56823bd13fee68999327c2033bbd046d12788ef`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 18.0 KB (17954 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1.0.2-18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:366ed2adfdff5a80a5ba4dc2cda1292e11dd573d56c95b23fd7527d0abd57e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58604475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1133e12468c7959d2d714dc1278b56a843d9a62239ebee8cec8ae38b74443137`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c65f6bdf4051cd9c6f061b0cfda47467e3e58b16f74111cfd422f71de36f2f`  
		Last Modified: Tue, 21 May 2024 18:57:15 GMT  
		Size: 39.4 MB (39358407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ee6393f192419546b9f3e7c2a1dbf1e0cbb9ce899e97047710f672faa393c0`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 1.4 MB (1382328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5ec9da9bc085a79e5149ae99c65b3a4529a919d2d461bf77c6470176657763`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f541ec1a406728e856fa42c9c07bc7ec105c26f480f421bc5798b4a80970c82b`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 886.9 KB (886907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a17d49bb7c9b1c155f629f8aafbf911967fb0c524217fde3e1265650e2883d6`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa624262f6c2c0374cdf88f907432420ea08c1853c5080bd2a94732fcacbafb`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 13.6 MB (13642080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d515a8401de5b09984be00337670c33c2b0f1531b44941b1252a112aac3943`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0.2-18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:1655dca624bd69180fb3a1517213cf766615e6f09654f909af74c562e61df657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.8 KB (871770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1e80e7198b9208ccc52fb3785bddaf5b948e1a3a3bc5dd6c8e998a9443bfc5`

```dockerfile
```

-	Layers:
	-	`sha256:0b5697ffa03ecd3e2d95c8f764886160a2f93212c0c552e5367c4930e7fe348e`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 853.8 KB (853794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14823bc6c9262151451390e9542239a27c7fc35b8b784ef2167081a33461b4ed`  
		Last Modified: Wed, 22 May 2024 01:27:36 GMT  
		Size: 18.0 KB (17976 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1.0.2-18-alpine3.18`

```console
$ docker pull mongo-express@sha256:1b23d7976f0210dbec74045c209e52fbb26d29b2e873d6c6fa3d3f0ae32c2a64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1.0.2-18-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:16ec1773958dcc4baa97c9256ef36cb537f6fa86343f4d8b2eb65e174bdd13c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58932530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870141b735e7d896bde590765c341cdc64fb6d3284b5f6a81f70ec936e4d0b83`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a007eb24b0933d3275c67be086dc77622f1ff9832cd958c1e95c151f1a8a5`  
		Last Modified: Tue, 21 May 2024 17:38:21 GMT  
		Size: 39.7 MB (39701778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5189255e31c875046be6a3ece5ca5f1a54e136a8c8cba93e4e1bd790a5abe895`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 1.4 MB (1382340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4f8a6bc8d94f7f9fc9369452ba43b1da76575ce6afb0c273625b964aa59b2`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8305ae32c9545d17c51422ec6988c967b85c2ee1325fa52a21d4262dc00b2f8`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 802.3 KB (802260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b24ec126f9adddbf26755ef3d6e6018db3130be0a4351dc633de2be6f060a6`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7f59574f7db0afb123e92393fd591943720ba8325e2a93968ac03207463da9`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 13.6 MB (13642215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf3571b6cd74d1ca8d070d1eb0094fc337ca653706461fb355e6dc926087149`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0.2-18-alpine3.18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:413b1ec7d1063aa5d4c956b0c6a2bd41f2842c9e4bed60f2cf3630a300e7d419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.7 KB (871725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d93d63e9f733ec2ba4bdc53527eaeaaaacfb672032150579facdb0b05465ed`

```dockerfile
```

-	Layers:
	-	`sha256:99ef4db52d2b92160459751d6e67f7e46f3c8290ebdf5690ece278383f611ed5`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 853.8 KB (853771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337574bd0f5e62ff1a58c6c8e56823bd13fee68999327c2033bbd046d12788ef`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 18.0 KB (17954 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1.0.2-18-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:366ed2adfdff5a80a5ba4dc2cda1292e11dd573d56c95b23fd7527d0abd57e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58604475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1133e12468c7959d2d714dc1278b56a843d9a62239ebee8cec8ae38b74443137`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c65f6bdf4051cd9c6f061b0cfda47467e3e58b16f74111cfd422f71de36f2f`  
		Last Modified: Tue, 21 May 2024 18:57:15 GMT  
		Size: 39.4 MB (39358407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ee6393f192419546b9f3e7c2a1dbf1e0cbb9ce899e97047710f672faa393c0`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 1.4 MB (1382328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5ec9da9bc085a79e5149ae99c65b3a4529a919d2d461bf77c6470176657763`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f541ec1a406728e856fa42c9c07bc7ec105c26f480f421bc5798b4a80970c82b`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 886.9 KB (886907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a17d49bb7c9b1c155f629f8aafbf911967fb0c524217fde3e1265650e2883d6`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa624262f6c2c0374cdf88f907432420ea08c1853c5080bd2a94732fcacbafb`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 13.6 MB (13642080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d515a8401de5b09984be00337670c33c2b0f1531b44941b1252a112aac3943`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0.2-18-alpine3.18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:1655dca624bd69180fb3a1517213cf766615e6f09654f909af74c562e61df657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.8 KB (871770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1e80e7198b9208ccc52fb3785bddaf5b948e1a3a3bc5dd6c8e998a9443bfc5`

```dockerfile
```

-	Layers:
	-	`sha256:0b5697ffa03ecd3e2d95c8f764886160a2f93212c0c552e5367c4930e7fe348e`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 853.8 KB (853794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14823bc6c9262151451390e9542239a27c7fc35b8b784ef2167081a33461b4ed`  
		Last Modified: Wed, 22 May 2024 01:27:36 GMT  
		Size: 18.0 KB (17976 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1.0.2-18-alpine3.19`

```console
$ docker pull mongo-express@sha256:f2cb0f0ba1ce096c7401cfdccd025c4bc0684491cb0525e71546a6885486d32d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1.0.2-18-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:d5c18b7bf513dfa964190c6426cb5e1efc29b7202e71d0a7391fdc8dc94475a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59061137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342f2aca699c73e5f47e2c31368b0f49e959b6eef7ae6dfa74b3796bab26995a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.4
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
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
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bfd1a7f5d0b2ad6106b6097bf76f56d3a8c3bcc5cf7fa1f5d0a0ca9dc32cbc`  
		Last Modified: Mon, 22 Jul 2024 23:05:40 GMT  
		Size: 39.8 MB (39831284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f16a148263d04e03d25d24411a9a48c71d7e31131900f4110b45b53c5a23ec`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 1.4 MB (1382231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30aa900b096c1999e57347eefc256ac6d0f228a2427efa4b8d9b2ec9152e74`  
		Last Modified: Mon, 22 Jul 2024 23:05:39 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169da638993ed85f93c9e80244f3c282973a5d0ec0ecbb326127de99bf259310`  
		Last Modified: Tue, 23 Jul 2024 00:09:11 GMT  
		Size: 784.6 KB (784639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183fe892943f23a74e750a64320c615f2a2746c5b846b9af2b5fab8bd95d20d3`  
		Last Modified: Tue, 23 Jul 2024 00:09:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a85f23501d9ddab32f11f2c379b60ed3a2e68da4d6274d6eb71d2776d62912`  
		Last Modified: Tue, 23 Jul 2024 00:09:12 GMT  
		Size: 13.6 MB (13642551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9a502d228384829f99ad2dbcbcb0a8067c0428d7f3d9d2ddf81965f8fa66f9`  
		Last Modified: Tue, 23 Jul 2024 00:09:11 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0.2-18-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:c4516269454877faf8c9692692b8a5496db8224ce01447ff300a5785f5dd19c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **952.4 KB (952382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07b786262bf0f0ba037b7e4a3b30acb1d842c6a1721c00598ca85c4ca15e166`

```dockerfile
```

-	Layers:
	-	`sha256:1687d253fb1176af9a484de43a19f21d7b95f56a9ef8e7ba2e65f26adcfd21a2`  
		Last Modified: Tue, 23 Jul 2024 00:09:11 GMT  
		Size: 937.1 KB (937118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcaf346464aea6b9ddb151968a41923bdb5e2e1a01b7fd4ce21d51a54db0fa7d`  
		Last Modified: Tue, 23 Jul 2024 00:09:11 GMT  
		Size: 15.3 KB (15264 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1.0.2-18-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:1917bfbd072111e6787c0d7671b70db1c48b5dedc8575d59980480a8668f0f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58784798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e9ea620d2df5f8d1ff60dbd50179071636ea950a054fcd17ec74c1a4443b9c`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.4
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="ac4fe3bef38d5e4ecf172b46c8af1f346904afd9788ce12919e3696f601e191e" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
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
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d34fa575f3bac771ddb2aa598addd06eb8ee9021b249cbc0e60e5e9cd74885c`  
		Last Modified: Tue, 23 Jul 2024 21:29:17 GMT  
		Size: 39.5 MB (39537820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8ada097bad821da4edbdb4753ce1e3ca5ddf992a4bac4a2f723b4819ac2d96`  
		Last Modified: Tue, 23 Jul 2024 21:29:17 GMT  
		Size: 1.4 MB (1382238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae55db9b5c5d4ef1702f1307c5604009843d2a03b7e3b4d1e671c0d3c95abf7`  
		Last Modified: Tue, 23 Jul 2024 21:29:16 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3898847d95ac7116957cf14cf5dd521d07bf1b44db7d55981c543164bf297c69`  
		Last Modified: Wed, 24 Jul 2024 16:00:15 GMT  
		Size: 862.4 KB (862434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c176ed9423f7e5dd1d530f4a6d1b9a60e9b5569566c45d7e65ca4dc5f07c64d`  
		Last Modified: Wed, 24 Jul 2024 16:00:14 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a231052b9eefc4c140d03c6d5f3cf634b9bb0fa38dfe501968843a6ff5ed59`  
		Last Modified: Wed, 24 Jul 2024 16:00:15 GMT  
		Size: 13.6 MB (13642459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce42b3807b6cc5b97526394a23af24e77bb35e19cc16b9dc3009bfe62b025b51`  
		Last Modified: Wed, 24 Jul 2024 16:00:14 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0.2-18-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:c827c59edcc29da428f7166481dd93ab56fb1c6467af525653473bf857c2067a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **952.8 KB (952829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e072a88d682d05035a2450fbe7c4ce1db321ac4083f9e0bdb19faf34f3e9d16`

```dockerfile
```

-	Layers:
	-	`sha256:9acdc47665608bbd190c9f2027affe013283907502482a7ace623d6dd3642cfb`  
		Last Modified: Wed, 24 Jul 2024 16:00:15 GMT  
		Size: 937.2 KB (937162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51a2bf33c3415b297374606c92d9214c5a62aafe68b47aa52e90e8ef3844b1b2`  
		Last Modified: Wed, 24 Jul 2024 16:00:14 GMT  
		Size: 15.7 KB (15667 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1.0.2-20`

```console
$ docker pull mongo-express@sha256:30fc6333779340217c6a2bc0bc3cd53aa46028ab8fc6caef41bd00bf0faacf53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1.0.2-20` - linux; amd64

```console
$ docker pull mongo-express@sha256:4efb9d899e2df08c2376e34d56d9540a8df8b6a77eb6494f7b99be2d33b7fa6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61319803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6389604d11ffa3b080a5dc390ee48f080dc3d6ba840f4ee700d55db6026460d`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.13.1
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a723c5566edc88aa2d53704f40a8be5984a6bb1eeac2d952577c8a13b6aacb7b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f45eb22fa20b605d639b56c941eee09d35f22e3308138f9ca549682f1ca3709`  
		Last Modified: Thu, 09 May 2024 19:33:09 GMT  
		Size: 42.1 MB (42090948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c695c2a88c4c3a8f44d4dcbbe13fe8035850eed2d96d550d162ac2494ce1057`  
		Last Modified: Thu, 09 May 2024 19:33:03 GMT  
		Size: 1.4 MB (1382339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb35f839ffe35efef3413fa7d570e3b7f760e058e0ce4e2d559a6cfeef49ed2d`  
		Last Modified: Thu, 09 May 2024 19:33:03 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6760b677c65af4266d44d87a523b05b4a46fd1f2cd629d823e2b32d87736e5c`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 802.3 KB (802254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d870e531048239a7f00267838e7b7aa1a6521b1327ba9af44f2e183933cc3bc9`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0923af95f273ca96c5940f7fdb8dd894937675f7356c2f3d0c070ad64f3383`  
		Last Modified: Thu, 16 May 2024 21:17:41 GMT  
		Size: 13.6 MB (13640323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d591368a3ca459ae6b7ff4033bf6ecca1ca6b106cf4c873f7ffb6cf63b37956e`  
		Last Modified: Thu, 16 May 2024 21:17:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0.2-20` - unknown; unknown

```console
$ docker pull mongo-express@sha256:565f13d8fadcbc6339e7121f3a8bc22928659ff487338fb0fa9fcb71ec26aacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.2 KB (886250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75571567217624a0844467488c2ce51dc84aa41ac797431a3687bd519c6ed811`

```dockerfile
```

-	Layers:
	-	`sha256:384104d98c8c6327d8f0d8eafa856e2d67dc0afc729fed151aadef3d148e9766`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 869.5 KB (869526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428d1351fe0d5ab05317464cecc0248d9252bfbe39ad0bd36a3d2d2de94ac229`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 16.7 KB (16724 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1.0.2-20` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:61595f75f159e417270c976ca6ab7393ee3c734a930a7cc500b916ee1668d627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61086108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683f152e5af50adb0da95d01bdc58abfd463e14fcd33ac40445db458a937e855`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.13.1
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a723c5566edc88aa2d53704f40a8be5984a6bb1eeac2d952577c8a13b6aacb7b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79650a799acd01e8d1e1c75528816262c35bd29243bc36a6ef8c5fc119fbd452`  
		Last Modified: Thu, 09 May 2024 20:33:48 GMT  
		Size: 41.8 MB (41841782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2dc15869135031a1f26ac2fa8e6ead18a4ad8e4c5dcc08ffcf30b2e81d6f27`  
		Last Modified: Thu, 09 May 2024 20:33:44 GMT  
		Size: 1.4 MB (1382319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6bbcfe9ab8b72380fc1c1f4dabb2fb18dd5d1fb8c18f4c81e21a76dc563420`  
		Last Modified: Thu, 09 May 2024 20:33:43 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda9e6789178b6ca1e8f50340a02cc6ca3ea258c2b4e596333c45b130b891d9`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 886.9 KB (886915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81bf146f4e81f2aff2340a2041e79f94a81540c7d16a7c2becc72e4b780103f`  
		Last Modified: Thu, 16 May 2024 23:39:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacfc2ffce94d32dd6677e37c45532046c23dbb4b2183d51b9202aeb51a0b66`  
		Last Modified: Thu, 16 May 2024 23:39:28 GMT  
		Size: 13.6 MB (13640341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6391dab4f4159f0f7c4c965dc2b8155acb25f3f401394c7ae6479d7db60f8e`  
		Last Modified: Thu, 16 May 2024 23:39:28 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0.2-20` - unknown; unknown

```console
$ docker pull mongo-express@sha256:726b54d4dbfbc3441cfed9dc5201370dd8ee05797523031f07fbedec5ab2262a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.3 KB (886277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c57ff4134182ff8945e2395e790022f7c6c2a6f043fb14dee74fd226b290ea`

```dockerfile
```

-	Layers:
	-	`sha256:a6a026c6678809f55212fb61571eff769609c21fb067cd587fe4d4f4006fe4fa`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 869.5 KB (869541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0c143a0a869c3080e8ae773c180060a4a88ec6940e736947d1cbec45d0c74b`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 16.7 KB (16736 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1.0.2-20-alpine3.18`

```console
$ docker pull mongo-express@sha256:30fc6333779340217c6a2bc0bc3cd53aa46028ab8fc6caef41bd00bf0faacf53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1.0.2-20-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:4efb9d899e2df08c2376e34d56d9540a8df8b6a77eb6494f7b99be2d33b7fa6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61319803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6389604d11ffa3b080a5dc390ee48f080dc3d6ba840f4ee700d55db6026460d`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.13.1
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a723c5566edc88aa2d53704f40a8be5984a6bb1eeac2d952577c8a13b6aacb7b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f45eb22fa20b605d639b56c941eee09d35f22e3308138f9ca549682f1ca3709`  
		Last Modified: Thu, 09 May 2024 19:33:09 GMT  
		Size: 42.1 MB (42090948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c695c2a88c4c3a8f44d4dcbbe13fe8035850eed2d96d550d162ac2494ce1057`  
		Last Modified: Thu, 09 May 2024 19:33:03 GMT  
		Size: 1.4 MB (1382339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb35f839ffe35efef3413fa7d570e3b7f760e058e0ce4e2d559a6cfeef49ed2d`  
		Last Modified: Thu, 09 May 2024 19:33:03 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6760b677c65af4266d44d87a523b05b4a46fd1f2cd629d823e2b32d87736e5c`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 802.3 KB (802254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d870e531048239a7f00267838e7b7aa1a6521b1327ba9af44f2e183933cc3bc9`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0923af95f273ca96c5940f7fdb8dd894937675f7356c2f3d0c070ad64f3383`  
		Last Modified: Thu, 16 May 2024 21:17:41 GMT  
		Size: 13.6 MB (13640323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d591368a3ca459ae6b7ff4033bf6ecca1ca6b106cf4c873f7ffb6cf63b37956e`  
		Last Modified: Thu, 16 May 2024 21:17:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0.2-20-alpine3.18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:565f13d8fadcbc6339e7121f3a8bc22928659ff487338fb0fa9fcb71ec26aacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.2 KB (886250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75571567217624a0844467488c2ce51dc84aa41ac797431a3687bd519c6ed811`

```dockerfile
```

-	Layers:
	-	`sha256:384104d98c8c6327d8f0d8eafa856e2d67dc0afc729fed151aadef3d148e9766`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 869.5 KB (869526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428d1351fe0d5ab05317464cecc0248d9252bfbe39ad0bd36a3d2d2de94ac229`  
		Last Modified: Thu, 16 May 2024 21:17:40 GMT  
		Size: 16.7 KB (16724 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1.0.2-20-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:61595f75f159e417270c976ca6ab7393ee3c734a930a7cc500b916ee1668d627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61086108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683f152e5af50adb0da95d01bdc58abfd463e14fcd33ac40445db458a937e855`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.13.1
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a723c5566edc88aa2d53704f40a8be5984a6bb1eeac2d952577c8a13b6aacb7b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79650a799acd01e8d1e1c75528816262c35bd29243bc36a6ef8c5fc119fbd452`  
		Last Modified: Thu, 09 May 2024 20:33:48 GMT  
		Size: 41.8 MB (41841782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2dc15869135031a1f26ac2fa8e6ead18a4ad8e4c5dcc08ffcf30b2e81d6f27`  
		Last Modified: Thu, 09 May 2024 20:33:44 GMT  
		Size: 1.4 MB (1382319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6bbcfe9ab8b72380fc1c1f4dabb2fb18dd5d1fb8c18f4c81e21a76dc563420`  
		Last Modified: Thu, 09 May 2024 20:33:43 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda9e6789178b6ca1e8f50340a02cc6ca3ea258c2b4e596333c45b130b891d9`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 886.9 KB (886915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81bf146f4e81f2aff2340a2041e79f94a81540c7d16a7c2becc72e4b780103f`  
		Last Modified: Thu, 16 May 2024 23:39:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eacfc2ffce94d32dd6677e37c45532046c23dbb4b2183d51b9202aeb51a0b66`  
		Last Modified: Thu, 16 May 2024 23:39:28 GMT  
		Size: 13.6 MB (13640341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6391dab4f4159f0f7c4c965dc2b8155acb25f3f401394c7ae6479d7db60f8e`  
		Last Modified: Thu, 16 May 2024 23:39:28 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0.2-20-alpine3.18` - unknown; unknown

```console
$ docker pull mongo-express@sha256:726b54d4dbfbc3441cfed9dc5201370dd8ee05797523031f07fbedec5ab2262a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.3 KB (886277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c57ff4134182ff8945e2395e790022f7c6c2a6f043fb14dee74fd226b290ea`

```dockerfile
```

-	Layers:
	-	`sha256:a6a026c6678809f55212fb61571eff769609c21fb067cd587fe4d4f4006fe4fa`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 869.5 KB (869541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0c143a0a869c3080e8ae773c180060a4a88ec6940e736947d1cbec45d0c74b`  
		Last Modified: Thu, 16 May 2024 23:39:26 GMT  
		Size: 16.7 KB (16736 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:1.0.2-20-alpine3.19`

```console
$ docker pull mongo-express@sha256:b47630179d52a780c65cc547503d7953a4ac3f791eaa9d4e8f61243f6da54aa7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1.0.2-20-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:58a8b49f0c9abaf0f1ba430be1202e891d51402c2ab8383c733838fdccfead67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61478686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e136336c2760eeb853bcfd31f35924ca0d85d29aa1832396342fc1a4cb50528b`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.16.0
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="40efcec63e42ca58a39cc89c99d8852bd31ea09e046966b321fd337be999651d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
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
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec6334b9b0a790105fc39fe11022bb7c8b844a2c7e07b8bde337b7f4ff0c7df`  
		Last Modified: Wed, 24 Jul 2024 15:04:16 GMT  
		Size: 42.2 MB (42246294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8508bfb40de7bd1b0ef262a221277657f56967f8b948c757db72f7c4f4bddcf`  
		Last Modified: Wed, 24 Jul 2024 15:04:15 GMT  
		Size: 1.4 MB (1387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1368777c2a4047a6257f340e9d9b4d0a8e48ee04031b04f2754455a2348b9ada`  
		Last Modified: Wed, 24 Jul 2024 15:04:14 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0c462386bc3775c2812b964c489638c7f71254d3f3bbdcf51d2b902d0b2b1e`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 784.7 KB (784651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5e5b3c85d0bf7718ec6b944641d9ec27d34e69468d0d39ee74091e8b53c3b5`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be7b6ef8947ba420191f6792fcf34960cd81c6c61f3163999e36636cc928c42`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 13.6 MB (13640089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc9da1a3da68b8538b549b171acbb3b3aab0e2c0efcba0d6ee2c1060ef13c55`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0.2-20-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:ab4548921cc928d8da7887ef88674cd70f5c5724d4b731fcb6b1efa7d0c41c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.9 KB (949881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1462946f370d02614aa083d2ac23608b6f88ce73e40ea9808a810400be4d605f`

```dockerfile
```

-	Layers:
	-	`sha256:b691f14cb639c942f583b3971e036f265d0ad849cdd0a2e4bd514af329a71238`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 934.6 KB (934617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f273552636b43c575cdcad65d7c6d95e419b9c49ba68507afb546ef44f218a`  
		Last Modified: Wed, 24 Jul 2024 15:55:59 GMT  
		Size: 15.3 KB (15264 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1.0.2-20-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:66c693e57b78054d86a6088b1c2c8b4ddc9ba703cc7b66bcbbb9aa25728abc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61253372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66be16b21a747d26cb07888f6fce278e5b2a6a4aaa0034703555bee9d568e735`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.15.1
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a5263215500d0f53e4b5194791bb8753df2380977d603bf408f5bf897eaf0708" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
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
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8843ec14bb10ffc4526ea83f602e1539ee1ad3e50edf6b230548256d2e0471cd`  
		Last Modified: Tue, 09 Jul 2024 18:06:51 GMT  
		Size: 42.0 MB (42005159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1708aba65ae6b8151fc0769578a456a6dca12c3d591792ca4f27c1fc233d8b74`  
		Last Modified: Tue, 09 Jul 2024 18:06:50 GMT  
		Size: 1.4 MB (1387218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a34874eeafb2834712acef30c3588dad8614613833c11b0aadc655efb5fd97`  
		Last Modified: Tue, 09 Jul 2024 18:06:49 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc10fc459286d0eefdfd555f366630cb94bc79b8299ed733a71379b3452fb7cf`  
		Last Modified: Tue, 09 Jul 2024 20:45:55 GMT  
		Size: 862.4 KB (862417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70706fc6c11bffbe80832642bdf80f88aa3e1427565b60a67d437b8ac5a1481`  
		Last Modified: Tue, 09 Jul 2024 20:45:55 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1a508ca4ad871393390beb5747c5112652bbd561e5893c8dfd6af24f1e2309`  
		Last Modified: Tue, 09 Jul 2024 20:45:55 GMT  
		Size: 13.6 MB (13639987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f4238113fc86b109d16ffcd8abb04bbb6232158245846a112a1d37ca03bff5`  
		Last Modified: Tue, 09 Jul 2024 20:45:55 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1.0.2-20-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:f05b4916fa918667d97f1e9aaa1999f3e250f30ba79ed2f6600850f4ac3347a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.8 KB (867802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f72482674dbc82edc9ccb33b3e10e6979a7dbf1f33156579b5584adc2e9df19`

```dockerfile
```

-	Layers:
	-	`sha256:0a0c792df95159c040e5177c7777e01688a678dacf8e9c0f8e0ace2ec5778dac`  
		Last Modified: Tue, 09 Jul 2024 20:45:54 GMT  
		Size: 852.1 KB (852135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e921a496e22ed15051735339925300b015e06a2a40df1a8c16c1111282cba06`  
		Last Modified: Tue, 09 Jul 2024 20:45:54 GMT  
		Size: 15.7 KB (15667 bytes)  
		MIME: application/vnd.in-toto+json

## `mongo-express:latest`

```console
$ docker pull mongo-express@sha256:1b23d7976f0210dbec74045c209e52fbb26d29b2e873d6c6fa3d3f0ae32c2a64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:latest` - linux; amd64

```console
$ docker pull mongo-express@sha256:16ec1773958dcc4baa97c9256ef36cb537f6fa86343f4d8b2eb65e174bdd13c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58932530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870141b735e7d896bde590765c341cdc64fb6d3284b5f6a81f70ec936e4d0b83`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a007eb24b0933d3275c67be086dc77622f1ff9832cd958c1e95c151f1a8a5`  
		Last Modified: Tue, 21 May 2024 17:38:21 GMT  
		Size: 39.7 MB (39701778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5189255e31c875046be6a3ece5ca5f1a54e136a8c8cba93e4e1bd790a5abe895`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 1.4 MB (1382340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4f8a6bc8d94f7f9fc9369452ba43b1da76575ce6afb0c273625b964aa59b2`  
		Last Modified: Tue, 21 May 2024 17:38:16 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8305ae32c9545d17c51422ec6988c967b85c2ee1325fa52a21d4262dc00b2f8`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 802.3 KB (802260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b24ec126f9adddbf26755ef3d6e6018db3130be0a4351dc633de2be6f060a6`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7f59574f7db0afb123e92393fd591943720ba8325e2a93968ac03207463da9`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 13.6 MB (13642215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf3571b6cd74d1ca8d070d1eb0094fc337ca653706461fb355e6dc926087149`  
		Last Modified: Tue, 21 May 2024 18:54:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:latest` - unknown; unknown

```console
$ docker pull mongo-express@sha256:413b1ec7d1063aa5d4c956b0c6a2bd41f2842c9e4bed60f2cf3630a300e7d419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.7 KB (871725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d93d63e9f733ec2ba4bdc53527eaeaaaacfb672032150579facdb0b05465ed`

```dockerfile
```

-	Layers:
	-	`sha256:99ef4db52d2b92160459751d6e67f7e46f3c8290ebdf5690ece278383f611ed5`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 853.8 KB (853771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337574bd0f5e62ff1a58c6c8e56823bd13fee68999327c2033bbd046d12788ef`  
		Last Modified: Tue, 21 May 2024 18:54:45 GMT  
		Size: 18.0 KB (17954 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:latest` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:366ed2adfdff5a80a5ba4dc2cda1292e11dd573d56c95b23fd7527d0abd57e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58604475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1133e12468c7959d2d714dc1278b56a843d9a62239ebee8cec8ae38b74443137`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.3
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3cfeaa3805cc424d1be0e281f0161416a99d206dcb589a9ab3647d7a6ab7d5c9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Fri, 08 Mar 2024 19:22:05 GMT
ENV YARN_VERSION=1.22.19
# Fri, 08 Mar 2024 19:22:05 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/*
# Fri, 08 Mar 2024 19:22:05 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c65f6bdf4051cd9c6f061b0cfda47467e3e58b16f74111cfd422f71de36f2f`  
		Last Modified: Tue, 21 May 2024 18:57:15 GMT  
		Size: 39.4 MB (39358407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ee6393f192419546b9f3e7c2a1dbf1e0cbb9ce899e97047710f672faa393c0`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 1.4 MB (1382328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5ec9da9bc085a79e5149ae99c65b3a4529a919d2d461bf77c6470176657763`  
		Last Modified: Tue, 21 May 2024 18:57:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f541ec1a406728e856fa42c9c07bc7ec105c26f480f421bc5798b4a80970c82b`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 886.9 KB (886907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a17d49bb7c9b1c155f629f8aafbf911967fb0c524217fde3e1265650e2883d6`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa624262f6c2c0374cdf88f907432420ea08c1853c5080bd2a94732fcacbafb`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 13.6 MB (13642080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d515a8401de5b09984be00337670c33c2b0f1531b44941b1252a112aac3943`  
		Last Modified: Wed, 22 May 2024 01:27:38 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:latest` - unknown; unknown

```console
$ docker pull mongo-express@sha256:1655dca624bd69180fb3a1517213cf766615e6f09654f909af74c562e61df657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.8 KB (871770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1e80e7198b9208ccc52fb3785bddaf5b948e1a3a3bc5dd6c8e998a9443bfc5`

```dockerfile
```

-	Layers:
	-	`sha256:0b5697ffa03ecd3e2d95c8f764886160a2f93212c0c552e5367c4930e7fe348e`  
		Last Modified: Wed, 22 May 2024 01:27:37 GMT  
		Size: 853.8 KB (853794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14823bc6c9262151451390e9542239a27c7fc35b8b784ef2167081a33461b4ed`  
		Last Modified: Wed, 22 May 2024 01:27:36 GMT  
		Size: 18.0 KB (17976 bytes)  
		MIME: application/vnd.in-toto+json

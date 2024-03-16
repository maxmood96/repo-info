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
$ docker pull mongo-express@sha256:66dfa6a39deffce1935669807d205eca3edd7a8459c701ffe75d7e3e81df10ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1` - linux; amd64

```console
$ docker pull mongo-express@sha256:7350263cc85ce61aee73dac649094ebbdb3312e72d7b8730ad6dd4fecf52c8cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79723055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3c796960930a5f7ca3e7f324513a1d17f244fac1fe6b43f401385b7a4dcd9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:31:30 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 03:31:39 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:39 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:31:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:31:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:31:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:31:44 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:51:34 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:51:34 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:51:34 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:51:35 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:52:12 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:52:13 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:52:13 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:52:13 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:52:14 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:52:14 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bbeb28556ec2281a75a0dd28eac89ea4e8061f158b8d46fbd152a65d941a45`  
		Last Modified: Sat, 16 Mar 2024 03:35:27 GMT  
		Size: 40.1 MB (40110896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c579a9bd17009e90ba555dd059d4888d47caba34c05aa588d1be8eb99be497a4`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 2.3 MB (2342667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745a187ebdeee71b739cc7f33b1ed13c1e1721e22582bfef4056e8d16079a1f0`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f3c466a5e17fe5795a69aa5d28fea1309438865e867612227cdcf4e37546cd`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d198b3ae6a7adbe6be3f69aaeec427b4a3606ef39536b2cc08b4bd61260360`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba939722952f2a818595b15a63a2c30f0c524d72d96405589b812d1df53667c`  
		Last Modified: Sat, 16 Mar 2024 12:53:42 GMT  
		Size: 33.1 MB (33063206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc31ad8151e1f2e180ff57a1787d64518a0fe2cd8c27e78449dffba372cd40d8`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:9b6c71eab90311187fb40dc7addde1d9dc0624209e18bfff0b574bba8b226630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79442831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9901baf84d44edc45f517e508bd308d43a9c4eedc168ea3c29e56b23f5de2a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:30:59 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 07:51:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:51:06 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:51:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:51:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:51:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:51:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:25:30 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:25:30 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:25:30 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:25:31 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:26:03 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:26:05 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:26:05 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:26:05 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:26:05 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:26:05 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba3ec755ffa1858566fb0656750edff534b6ed03c9078392fb0c19cb10b4f8d`  
		Last Modified: Sat, 16 Mar 2024 08:14:10 GMT  
		Size: 39.8 MB (39816343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dafbded8808a388313b6f83fb3ee6df3ba8ce31c7ba159dd5f660e2dde30581`  
		Last Modified: Sat, 16 Mar 2024 08:14:06 GMT  
		Size: 2.3 MB (2342589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4f9a3ef664bbf378ffcb5942bc44e7cd5e6b4d1c688cf44065e731fb903cb`  
		Last Modified: Sat, 16 Mar 2024 08:14:05 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fccb851668e56077568c2412f62d9dd8c4bd945c763e023e072acb7417630c0`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd1b4af91499eb4e0213faff62b10ae12243e4c43dd5bd5010bfa50cb65b20c`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d5141fd23193bb9201e4bd3cc5093b0fb10b1e2a2c0cc4c637b71db2fc6f3d`  
		Last Modified: Sat, 16 Mar 2024 13:27:23 GMT  
		Size: 33.1 MB (33062121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd0bcf46415de040e9ec87d689f9379e65d9049a254fa2f5a50f3a1dbb8bc5b`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1-18`

```console
$ docker pull mongo-express@sha256:66dfa6a39deffce1935669807d205eca3edd7a8459c701ffe75d7e3e81df10ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1-18` - linux; amd64

```console
$ docker pull mongo-express@sha256:7350263cc85ce61aee73dac649094ebbdb3312e72d7b8730ad6dd4fecf52c8cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79723055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3c796960930a5f7ca3e7f324513a1d17f244fac1fe6b43f401385b7a4dcd9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:31:30 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 03:31:39 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:39 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:31:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:31:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:31:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:31:44 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:51:34 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:51:34 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:51:34 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:51:35 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:52:12 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:52:13 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:52:13 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:52:13 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:52:14 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:52:14 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bbeb28556ec2281a75a0dd28eac89ea4e8061f158b8d46fbd152a65d941a45`  
		Last Modified: Sat, 16 Mar 2024 03:35:27 GMT  
		Size: 40.1 MB (40110896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c579a9bd17009e90ba555dd059d4888d47caba34c05aa588d1be8eb99be497a4`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 2.3 MB (2342667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745a187ebdeee71b739cc7f33b1ed13c1e1721e22582bfef4056e8d16079a1f0`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f3c466a5e17fe5795a69aa5d28fea1309438865e867612227cdcf4e37546cd`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d198b3ae6a7adbe6be3f69aaeec427b4a3606ef39536b2cc08b4bd61260360`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba939722952f2a818595b15a63a2c30f0c524d72d96405589b812d1df53667c`  
		Last Modified: Sat, 16 Mar 2024 12:53:42 GMT  
		Size: 33.1 MB (33063206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc31ad8151e1f2e180ff57a1787d64518a0fe2cd8c27e78449dffba372cd40d8`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1-18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:9b6c71eab90311187fb40dc7addde1d9dc0624209e18bfff0b574bba8b226630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79442831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9901baf84d44edc45f517e508bd308d43a9c4eedc168ea3c29e56b23f5de2a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:30:59 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 07:51:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:51:06 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:51:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:51:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:51:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:51:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:25:30 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:25:30 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:25:30 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:25:31 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:26:03 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:26:05 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:26:05 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:26:05 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:26:05 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:26:05 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba3ec755ffa1858566fb0656750edff534b6ed03c9078392fb0c19cb10b4f8d`  
		Last Modified: Sat, 16 Mar 2024 08:14:10 GMT  
		Size: 39.8 MB (39816343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dafbded8808a388313b6f83fb3ee6df3ba8ce31c7ba159dd5f660e2dde30581`  
		Last Modified: Sat, 16 Mar 2024 08:14:06 GMT  
		Size: 2.3 MB (2342589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4f9a3ef664bbf378ffcb5942bc44e7cd5e6b4d1c688cf44065e731fb903cb`  
		Last Modified: Sat, 16 Mar 2024 08:14:05 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fccb851668e56077568c2412f62d9dd8c4bd945c763e023e072acb7417630c0`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd1b4af91499eb4e0213faff62b10ae12243e4c43dd5bd5010bfa50cb65b20c`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d5141fd23193bb9201e4bd3cc5093b0fb10b1e2a2c0cc4c637b71db2fc6f3d`  
		Last Modified: Sat, 16 Mar 2024 13:27:23 GMT  
		Size: 33.1 MB (33062121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd0bcf46415de040e9ec87d689f9379e65d9049a254fa2f5a50f3a1dbb8bc5b`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1-18-alpine3.18`

```console
$ docker pull mongo-express@sha256:66dfa6a39deffce1935669807d205eca3edd7a8459c701ffe75d7e3e81df10ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1-18-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:7350263cc85ce61aee73dac649094ebbdb3312e72d7b8730ad6dd4fecf52c8cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79723055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3c796960930a5f7ca3e7f324513a1d17f244fac1fe6b43f401385b7a4dcd9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:31:30 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 03:31:39 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:39 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:31:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:31:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:31:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:31:44 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:51:34 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:51:34 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:51:34 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:51:35 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:52:12 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:52:13 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:52:13 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:52:13 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:52:14 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:52:14 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bbeb28556ec2281a75a0dd28eac89ea4e8061f158b8d46fbd152a65d941a45`  
		Last Modified: Sat, 16 Mar 2024 03:35:27 GMT  
		Size: 40.1 MB (40110896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c579a9bd17009e90ba555dd059d4888d47caba34c05aa588d1be8eb99be497a4`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 2.3 MB (2342667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745a187ebdeee71b739cc7f33b1ed13c1e1721e22582bfef4056e8d16079a1f0`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f3c466a5e17fe5795a69aa5d28fea1309438865e867612227cdcf4e37546cd`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d198b3ae6a7adbe6be3f69aaeec427b4a3606ef39536b2cc08b4bd61260360`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba939722952f2a818595b15a63a2c30f0c524d72d96405589b812d1df53667c`  
		Last Modified: Sat, 16 Mar 2024 12:53:42 GMT  
		Size: 33.1 MB (33063206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc31ad8151e1f2e180ff57a1787d64518a0fe2cd8c27e78449dffba372cd40d8`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1-18-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:9b6c71eab90311187fb40dc7addde1d9dc0624209e18bfff0b574bba8b226630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79442831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9901baf84d44edc45f517e508bd308d43a9c4eedc168ea3c29e56b23f5de2a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:30:59 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 07:51:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:51:06 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:51:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:51:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:51:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:51:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:25:30 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:25:30 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:25:30 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:25:31 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:26:03 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:26:05 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:26:05 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:26:05 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:26:05 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:26:05 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba3ec755ffa1858566fb0656750edff534b6ed03c9078392fb0c19cb10b4f8d`  
		Last Modified: Sat, 16 Mar 2024 08:14:10 GMT  
		Size: 39.8 MB (39816343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dafbded8808a388313b6f83fb3ee6df3ba8ce31c7ba159dd5f660e2dde30581`  
		Last Modified: Sat, 16 Mar 2024 08:14:06 GMT  
		Size: 2.3 MB (2342589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4f9a3ef664bbf378ffcb5942bc44e7cd5e6b4d1c688cf44065e731fb903cb`  
		Last Modified: Sat, 16 Mar 2024 08:14:05 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fccb851668e56077568c2412f62d9dd8c4bd945c763e023e072acb7417630c0`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd1b4af91499eb4e0213faff62b10ae12243e4c43dd5bd5010bfa50cb65b20c`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d5141fd23193bb9201e4bd3cc5093b0fb10b1e2a2c0cc4c637b71db2fc6f3d`  
		Last Modified: Sat, 16 Mar 2024 13:27:23 GMT  
		Size: 33.1 MB (33062121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd0bcf46415de040e9ec87d689f9379e65d9049a254fa2f5a50f3a1dbb8bc5b`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1-18-alpine3.19`

```console
$ docker pull mongo-express@sha256:9bbefb7db134c3fa06ffb90577316f73c1a1e9f0387280fe1bea437c5e47a92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1-18-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:293b21d1c1ca95a54eceba59f263161b0e642cbd72b57cc3c7cc3208b8ae259b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79847087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9232c24c4474e63f71c115ca7eae2b2273681845bf5bd34c4b5eb148c4dcc5d`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:31:48 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 03:31:56 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:57 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:32:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:32:02 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:32:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:32:02 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:50:45 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:50:45 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:50:45 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:50:45 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:51:22 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:51:24 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:51:24 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:51:24 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:51:24 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:51:24 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff171c16ee4e8ed3a0ae3edb6fb9558f281134a3879eedca7d79fc2e16e46073`  
		Last Modified: Sat, 16 Mar 2024 03:35:45 GMT  
		Size: 40.2 MB (40246754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c215e7ef3945bd4fdac5a20f1e4a29c62f28c8493ad05d3e651d62cf069140d`  
		Last Modified: Sat, 16 Mar 2024 03:35:39 GMT  
		Size: 2.3 MB (2342788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f72a72846173b6a02c1f73db9a74aca2af50fb39bf13ba2e4d12d13e5722d6c`  
		Last Modified: Sat, 16 Mar 2024 03:35:38 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5fc007d83ce2bea3e3e3e15b08c1941c5e7c244261d06bcf4f749c27679f2b`  
		Last Modified: Sat, 16 Mar 2024 12:53:17 GMT  
		Size: 784.7 KB (784714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dc20ed69fe2ba1321f8b6ca6be9ffa8256f6fa567d80f8a1fab80635ac6b9b`  
		Last Modified: Sat, 16 Mar 2024 12:53:17 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bed48b4f41b43763eb67104ba454968a725631dfcd68ffe875cf0aed2ed9b8e`  
		Last Modified: Sat, 16 Mar 2024 12:53:25 GMT  
		Size: 33.1 MB (33062676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8815f593fde212d510e4eb025d8f4f62b0a22a73e95ea68e7b31c1c8aeddde89`  
		Last Modified: Sat, 16 Mar 2024 12:53:17 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1-18-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:c0a6f6cc78eb16fdec4e25ce052ddf728f400dec8727bbd0c3fa5d6ca555de36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79616499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64f825c616364113e155c323b65b3aeac7654b0ebe20f99831d9f07e4025b11`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:51:22 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 08:11:07 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 08:11:07 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 08:11:12 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 08:11:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 08:11:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:11:12 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:24:50 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:24:50 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:24:50 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:24:51 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:25:23 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:25:25 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:25:25 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:25:25 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:25:25 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:25:25 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8657c71df119fa73d920b9e13c4d78e0b9c1ebcd073c3aec39cf36438d61231`  
		Last Modified: Sat, 16 Mar 2024 08:14:25 GMT  
		Size: 40.0 MB (39999911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048cf8cd15c8c1bdbd097e3168104729b5bdcffd2bbcd63b0124860f4fff0c21`  
		Last Modified: Sat, 16 Mar 2024 08:14:21 GMT  
		Size: 2.3 MB (2342746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ee200833ea33ad51efcd618903682b620e0d2cd420bc015a9c0a69ddc12a9e`  
		Last Modified: Sat, 16 Mar 2024 08:14:21 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c293927a519eba54163565007446d5418cbae0dcc7476b3d4a69e059e6a4406c`  
		Last Modified: Sat, 16 Mar 2024 13:27:01 GMT  
		Size: 862.4 KB (862436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c91c830721fda0245fc134f9d0b897126b7d854deead137939577abd8891640`  
		Last Modified: Sat, 16 Mar 2024 13:27:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a314aeac73211adfc52cd132c20b7861c8dee5d03d5ae441f8eea66d25605414`  
		Last Modified: Sat, 16 Mar 2024 13:27:07 GMT  
		Size: 33.1 MB (33062265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac137ed14914e03f924e95670d9be81b750765cb2d966d5188faee97982f14e`  
		Last Modified: Sat, 16 Mar 2024 13:27:01 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1-20`

```console
$ docker pull mongo-express@sha256:e621529902f686e864594a6db9948a64c4b022b3481c6ae2ec1f423f05eff15a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1-20` - linux; amd64

```console
$ docker pull mongo-express@sha256:ca06869055714bd880af47ebcba4345440b613605dcf463dd2375d909ca375f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81670554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef18415bc705b4e9e137f80183aebcd70d309715c710683aa28e74ecb6f4a66`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:30:36 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 03:30:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:30:46 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:30:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:30:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:30:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:30:51 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:49:56 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:49:56 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:49:56 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:49:56 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:50:33 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:50:34 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:50:34 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:50:34 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:50:34 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:50:35 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2a61871030542f55a6ec81ca7e2b393c7e3392e58a1fd97e5edfacd89918e2`  
		Last Modified: Sat, 16 Mar 2024 03:34:28 GMT  
		Size: 42.1 MB (42061773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243431d75724ed545c16e7216326878fbd58e429991be8dcca467107d144517`  
		Last Modified: Sat, 16 Mar 2024 03:34:22 GMT  
		Size: 2.3 MB (2341048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f042e74e78671927ad1a1d4ac10d69571054a09d0bce420d39ac4b857222a19`  
		Last Modified: Sat, 16 Mar 2024 03:34:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a4b4df73f1495ffa0079e4cd4ae221f2e13a9a0c676f1275d435b6e1aa7e10`  
		Last Modified: Sat, 16 Mar 2024 12:52:54 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a98bdbbeb961d54e068e47479f01ad7242d8eeb7d761f0fab69385695ec84d9`  
		Last Modified: Sat, 16 Mar 2024 12:52:53 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359f92ee7dd2c9e9f8d84548d57fbd10d0b29726e11f09c4dd34a575042f8732`  
		Last Modified: Sat, 16 Mar 2024 12:53:01 GMT  
		Size: 33.1 MB (33061447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c029ea17cdba5d5ac5448578edc7846dfdad17ab63c7a8844d6bcdc413ba98`  
		Last Modified: Sat, 16 Mar 2024 12:52:53 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1-20` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:01c3e3290cb8c4bf17bf766191d955a3b7c841ea5fe9cc4fa2878739e1be112a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81436380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236929dda6d6ad438b42a02149357f015f469d9a7009f3dc0e8582c501ded5ba`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:43:17 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 07:07:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:07:05 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:07:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:07:10 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:07:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:07:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:24:10 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:24:10 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:24:10 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:24:10 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:24:42 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:24:44 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:24:44 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:24:44 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:24:45 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:24:45 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014cc7646ef4d291a260436dd0c6949d8be2d31a1d562074b83222be1fc67c00`  
		Last Modified: Sat, 16 Mar 2024 08:13:13 GMT  
		Size: 41.8 MB (41812067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70242eaeabbd114d411d9a4e028012cf5a6603cbdcd6071c9a3cf98c712f01f`  
		Last Modified: Sat, 16 Mar 2024 08:13:09 GMT  
		Size: 2.3 MB (2340908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c48c4eabd9390f8a6b50d058cd1d4f09b299fa3d9e42a248c938b71c72c9212`  
		Last Modified: Sat, 16 Mar 2024 08:13:08 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047c003e3455e0498efd76e3b414efa7b3ee9dba486c3bca18f526b8e5475134`  
		Last Modified: Sat, 16 Mar 2024 13:26:39 GMT  
		Size: 887.0 KB (887003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dda267073c82524fa9a9b1ea5b8557db6e7b63f88a6d972b218ce9ac15138b`  
		Last Modified: Sat, 16 Mar 2024 13:26:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890347fa336e7376ea17ad33e269afe68b46193df94b4056440c70f6a92f17cb`  
		Last Modified: Sat, 16 Mar 2024 13:26:45 GMT  
		Size: 33.1 MB (33061618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a28b2b96503114222dfb0726756b780751497362797c05e8b56d3ff8e3701d`  
		Last Modified: Sat, 16 Mar 2024 13:26:38 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1-20-alpine3.18`

```console
$ docker pull mongo-express@sha256:e621529902f686e864594a6db9948a64c4b022b3481c6ae2ec1f423f05eff15a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1-20-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:ca06869055714bd880af47ebcba4345440b613605dcf463dd2375d909ca375f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81670554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef18415bc705b4e9e137f80183aebcd70d309715c710683aa28e74ecb6f4a66`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:30:36 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 03:30:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:30:46 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:30:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:30:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:30:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:30:51 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:49:56 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:49:56 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:49:56 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:49:56 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:50:33 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:50:34 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:50:34 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:50:34 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:50:34 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:50:35 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2a61871030542f55a6ec81ca7e2b393c7e3392e58a1fd97e5edfacd89918e2`  
		Last Modified: Sat, 16 Mar 2024 03:34:28 GMT  
		Size: 42.1 MB (42061773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243431d75724ed545c16e7216326878fbd58e429991be8dcca467107d144517`  
		Last Modified: Sat, 16 Mar 2024 03:34:22 GMT  
		Size: 2.3 MB (2341048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f042e74e78671927ad1a1d4ac10d69571054a09d0bce420d39ac4b857222a19`  
		Last Modified: Sat, 16 Mar 2024 03:34:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a4b4df73f1495ffa0079e4cd4ae221f2e13a9a0c676f1275d435b6e1aa7e10`  
		Last Modified: Sat, 16 Mar 2024 12:52:54 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a98bdbbeb961d54e068e47479f01ad7242d8eeb7d761f0fab69385695ec84d9`  
		Last Modified: Sat, 16 Mar 2024 12:52:53 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359f92ee7dd2c9e9f8d84548d57fbd10d0b29726e11f09c4dd34a575042f8732`  
		Last Modified: Sat, 16 Mar 2024 12:53:01 GMT  
		Size: 33.1 MB (33061447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c029ea17cdba5d5ac5448578edc7846dfdad17ab63c7a8844d6bcdc413ba98`  
		Last Modified: Sat, 16 Mar 2024 12:52:53 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1-20-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:01c3e3290cb8c4bf17bf766191d955a3b7c841ea5fe9cc4fa2878739e1be112a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81436380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236929dda6d6ad438b42a02149357f015f469d9a7009f3dc0e8582c501ded5ba`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:43:17 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 07:07:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:07:05 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:07:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:07:10 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:07:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:07:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:24:10 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:24:10 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:24:10 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:24:10 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:24:42 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:24:44 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:24:44 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:24:44 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:24:45 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:24:45 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014cc7646ef4d291a260436dd0c6949d8be2d31a1d562074b83222be1fc67c00`  
		Last Modified: Sat, 16 Mar 2024 08:13:13 GMT  
		Size: 41.8 MB (41812067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70242eaeabbd114d411d9a4e028012cf5a6603cbdcd6071c9a3cf98c712f01f`  
		Last Modified: Sat, 16 Mar 2024 08:13:09 GMT  
		Size: 2.3 MB (2340908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c48c4eabd9390f8a6b50d058cd1d4f09b299fa3d9e42a248c938b71c72c9212`  
		Last Modified: Sat, 16 Mar 2024 08:13:08 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047c003e3455e0498efd76e3b414efa7b3ee9dba486c3bca18f526b8e5475134`  
		Last Modified: Sat, 16 Mar 2024 13:26:39 GMT  
		Size: 887.0 KB (887003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dda267073c82524fa9a9b1ea5b8557db6e7b63f88a6d972b218ce9ac15138b`  
		Last Modified: Sat, 16 Mar 2024 13:26:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890347fa336e7376ea17ad33e269afe68b46193df94b4056440c70f6a92f17cb`  
		Last Modified: Sat, 16 Mar 2024 13:26:45 GMT  
		Size: 33.1 MB (33061618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a28b2b96503114222dfb0726756b780751497362797c05e8b56d3ff8e3701d`  
		Last Modified: Sat, 16 Mar 2024 13:26:38 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1-20-alpine3.19`

```console
$ docker pull mongo-express@sha256:64c3652d3d858bc670a6d6f4e1dcf372743d99286342581f84c79bd64aebd1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1-20-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:e51caebda20038d36a0a927945ac46982937830885d61f8365ff7f87da39c937
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81784162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e700d78696bd1f925f9ccf20b1570d85e2f237cb31d7d0f82d4313a14ed4c7`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:30:54 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 03:31:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:03 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:31:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:31:09 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:31:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:31:09 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:49:07 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:49:07 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:49:07 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:49:07 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:49:44 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:49:45 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:49:45 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:49:45 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:49:45 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:49:45 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f16480e2ff54481cb1ea1553429bf399e8269985ab0dec5b5af6f55ea747d3f`  
		Last Modified: Sat, 16 Mar 2024 03:34:48 GMT  
		Size: 42.2 MB (42186770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092226d52cac3f544d7973fe7ba4416bc2cd5b69e4016804efb95026fe6b108b`  
		Last Modified: Sat, 16 Mar 2024 03:34:41 GMT  
		Size: 2.3 MB (2341056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0493dfb2ff9c5bd770291dc14d4e30caff25c72bcdfbea04e9bf2f4013e21db0`  
		Last Modified: Sat, 16 Mar 2024 03:34:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ecd5787d8d96f063e89ed863d50acf522cf19bc960893428920be3e3f403e4`  
		Last Modified: Sat, 16 Mar 2024 12:52:36 GMT  
		Size: 784.7 KB (784709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef3edd5aece8b5458b4fec1593302b5d5a5f8e817968506db7dc59199097b0`  
		Last Modified: Sat, 16 Mar 2024 12:52:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852a8f6e0ae3bd255b309479997ea09526d64229d82dd929ff007dc63b397de0`  
		Last Modified: Sat, 16 Mar 2024 12:52:43 GMT  
		Size: 33.1 MB (33061473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beea5e3312ccc3a4a79efc11323b1946692f97158ba5c7f1a58fbd1b0d25947`  
		Last Modified: Sat, 16 Mar 2024 12:52:36 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1-20-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:eced3cdd6dcb4339b1255ece128faab3277ca31df13d139d8a3a6b16d9345477
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81627062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc62706911d7e3947b710307426dacfb496cdfe495e665a7e0376a39dc94e268`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:07:25 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 07:30:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:30:31 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:30:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:30:35 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:30:36 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:23:22 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:23:22 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:23:22 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:23:22 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:23:59 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:24:01 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:24:01 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:24:01 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:24:01 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:24:01 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93210f2a425301d4d76217e169b2005256fefe022ef4181715a590880a055162`  
		Last Modified: Sat, 16 Mar 2024 08:13:30 GMT  
		Size: 42.0 MB (42013649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef1c9a74cd88ae4dee8daee6d9a39425cb8411294789b3118317c9acc154648`  
		Last Modified: Sat, 16 Mar 2024 08:13:25 GMT  
		Size: 2.3 MB (2340967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bb1a28a290af7381f606e1a4492f0163ccbd60ee0daf41b43ffa0dd7d98676`  
		Last Modified: Sat, 16 Mar 2024 08:13:25 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1af0335e763361bf72725ef483ea81cc489a55273d74f649d71259497d7cbf`  
		Last Modified: Sat, 16 Mar 2024 13:26:22 GMT  
		Size: 862.4 KB (862443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449cfdb74fb98eb2a47fc6dd00edcc8959fcc9bf43c9b105dd6ad94513fc482d`  
		Last Modified: Sat, 16 Mar 2024 13:26:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0649943d1a66d3de1075fa69074fbba9f2984d6d9764a4c8dfaa0da83f9ec5`  
		Last Modified: Sat, 16 Mar 2024 13:26:28 GMT  
		Size: 33.1 MB (33060866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640ffa86d7bde36df864b1c5fb89700124947dfb5388a8d6e50f61701e47e1b6`  
		Last Modified: Sat, 16 Mar 2024 13:26:22 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0`

```console
$ docker pull mongo-express@sha256:66dfa6a39deffce1935669807d205eca3edd7a8459c701ffe75d7e3e81df10ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0` - linux; amd64

```console
$ docker pull mongo-express@sha256:7350263cc85ce61aee73dac649094ebbdb3312e72d7b8730ad6dd4fecf52c8cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79723055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3c796960930a5f7ca3e7f324513a1d17f244fac1fe6b43f401385b7a4dcd9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:31:30 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 03:31:39 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:39 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:31:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:31:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:31:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:31:44 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:51:34 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:51:34 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:51:34 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:51:35 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:52:12 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:52:13 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:52:13 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:52:13 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:52:14 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:52:14 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bbeb28556ec2281a75a0dd28eac89ea4e8061f158b8d46fbd152a65d941a45`  
		Last Modified: Sat, 16 Mar 2024 03:35:27 GMT  
		Size: 40.1 MB (40110896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c579a9bd17009e90ba555dd059d4888d47caba34c05aa588d1be8eb99be497a4`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 2.3 MB (2342667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745a187ebdeee71b739cc7f33b1ed13c1e1721e22582bfef4056e8d16079a1f0`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f3c466a5e17fe5795a69aa5d28fea1309438865e867612227cdcf4e37546cd`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d198b3ae6a7adbe6be3f69aaeec427b4a3606ef39536b2cc08b4bd61260360`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba939722952f2a818595b15a63a2c30f0c524d72d96405589b812d1df53667c`  
		Last Modified: Sat, 16 Mar 2024 12:53:42 GMT  
		Size: 33.1 MB (33063206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc31ad8151e1f2e180ff57a1787d64518a0fe2cd8c27e78449dffba372cd40d8`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:9b6c71eab90311187fb40dc7addde1d9dc0624209e18bfff0b574bba8b226630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79442831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9901baf84d44edc45f517e508bd308d43a9c4eedc168ea3c29e56b23f5de2a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:30:59 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 07:51:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:51:06 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:51:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:51:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:51:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:51:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:25:30 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:25:30 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:25:30 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:25:31 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:26:03 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:26:05 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:26:05 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:26:05 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:26:05 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:26:05 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba3ec755ffa1858566fb0656750edff534b6ed03c9078392fb0c19cb10b4f8d`  
		Last Modified: Sat, 16 Mar 2024 08:14:10 GMT  
		Size: 39.8 MB (39816343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dafbded8808a388313b6f83fb3ee6df3ba8ce31c7ba159dd5f660e2dde30581`  
		Last Modified: Sat, 16 Mar 2024 08:14:06 GMT  
		Size: 2.3 MB (2342589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4f9a3ef664bbf378ffcb5942bc44e7cd5e6b4d1c688cf44065e731fb903cb`  
		Last Modified: Sat, 16 Mar 2024 08:14:05 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fccb851668e56077568c2412f62d9dd8c4bd945c763e023e072acb7417630c0`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd1b4af91499eb4e0213faff62b10ae12243e4c43dd5bd5010bfa50cb65b20c`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d5141fd23193bb9201e4bd3cc5093b0fb10b1e2a2c0cc4c637b71db2fc6f3d`  
		Last Modified: Sat, 16 Mar 2024 13:27:23 GMT  
		Size: 33.1 MB (33062121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd0bcf46415de040e9ec87d689f9379e65d9049a254fa2f5a50f3a1dbb8bc5b`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0-18`

```console
$ docker pull mongo-express@sha256:66dfa6a39deffce1935669807d205eca3edd7a8459c701ffe75d7e3e81df10ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0-18` - linux; amd64

```console
$ docker pull mongo-express@sha256:7350263cc85ce61aee73dac649094ebbdb3312e72d7b8730ad6dd4fecf52c8cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79723055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3c796960930a5f7ca3e7f324513a1d17f244fac1fe6b43f401385b7a4dcd9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:31:30 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 03:31:39 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:39 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:31:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:31:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:31:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:31:44 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:51:34 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:51:34 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:51:34 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:51:35 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:52:12 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:52:13 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:52:13 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:52:13 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:52:14 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:52:14 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bbeb28556ec2281a75a0dd28eac89ea4e8061f158b8d46fbd152a65d941a45`  
		Last Modified: Sat, 16 Mar 2024 03:35:27 GMT  
		Size: 40.1 MB (40110896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c579a9bd17009e90ba555dd059d4888d47caba34c05aa588d1be8eb99be497a4`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 2.3 MB (2342667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745a187ebdeee71b739cc7f33b1ed13c1e1721e22582bfef4056e8d16079a1f0`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f3c466a5e17fe5795a69aa5d28fea1309438865e867612227cdcf4e37546cd`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d198b3ae6a7adbe6be3f69aaeec427b4a3606ef39536b2cc08b4bd61260360`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba939722952f2a818595b15a63a2c30f0c524d72d96405589b812d1df53667c`  
		Last Modified: Sat, 16 Mar 2024 12:53:42 GMT  
		Size: 33.1 MB (33063206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc31ad8151e1f2e180ff57a1787d64518a0fe2cd8c27e78449dffba372cd40d8`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0-18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:9b6c71eab90311187fb40dc7addde1d9dc0624209e18bfff0b574bba8b226630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79442831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9901baf84d44edc45f517e508bd308d43a9c4eedc168ea3c29e56b23f5de2a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:30:59 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 07:51:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:51:06 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:51:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:51:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:51:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:51:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:25:30 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:25:30 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:25:30 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:25:31 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:26:03 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:26:05 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:26:05 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:26:05 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:26:05 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:26:05 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba3ec755ffa1858566fb0656750edff534b6ed03c9078392fb0c19cb10b4f8d`  
		Last Modified: Sat, 16 Mar 2024 08:14:10 GMT  
		Size: 39.8 MB (39816343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dafbded8808a388313b6f83fb3ee6df3ba8ce31c7ba159dd5f660e2dde30581`  
		Last Modified: Sat, 16 Mar 2024 08:14:06 GMT  
		Size: 2.3 MB (2342589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4f9a3ef664bbf378ffcb5942bc44e7cd5e6b4d1c688cf44065e731fb903cb`  
		Last Modified: Sat, 16 Mar 2024 08:14:05 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fccb851668e56077568c2412f62d9dd8c4bd945c763e023e072acb7417630c0`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd1b4af91499eb4e0213faff62b10ae12243e4c43dd5bd5010bfa50cb65b20c`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d5141fd23193bb9201e4bd3cc5093b0fb10b1e2a2c0cc4c637b71db2fc6f3d`  
		Last Modified: Sat, 16 Mar 2024 13:27:23 GMT  
		Size: 33.1 MB (33062121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd0bcf46415de040e9ec87d689f9379e65d9049a254fa2f5a50f3a1dbb8bc5b`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0-18-alpine3.18`

```console
$ docker pull mongo-express@sha256:66dfa6a39deffce1935669807d205eca3edd7a8459c701ffe75d7e3e81df10ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0-18-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:7350263cc85ce61aee73dac649094ebbdb3312e72d7b8730ad6dd4fecf52c8cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79723055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3c796960930a5f7ca3e7f324513a1d17f244fac1fe6b43f401385b7a4dcd9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:31:30 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 03:31:39 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:39 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:31:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:31:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:31:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:31:44 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:51:34 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:51:34 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:51:34 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:51:35 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:52:12 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:52:13 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:52:13 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:52:13 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:52:14 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:52:14 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bbeb28556ec2281a75a0dd28eac89ea4e8061f158b8d46fbd152a65d941a45`  
		Last Modified: Sat, 16 Mar 2024 03:35:27 GMT  
		Size: 40.1 MB (40110896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c579a9bd17009e90ba555dd059d4888d47caba34c05aa588d1be8eb99be497a4`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 2.3 MB (2342667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745a187ebdeee71b739cc7f33b1ed13c1e1721e22582bfef4056e8d16079a1f0`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f3c466a5e17fe5795a69aa5d28fea1309438865e867612227cdcf4e37546cd`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d198b3ae6a7adbe6be3f69aaeec427b4a3606ef39536b2cc08b4bd61260360`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba939722952f2a818595b15a63a2c30f0c524d72d96405589b812d1df53667c`  
		Last Modified: Sat, 16 Mar 2024 12:53:42 GMT  
		Size: 33.1 MB (33063206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc31ad8151e1f2e180ff57a1787d64518a0fe2cd8c27e78449dffba372cd40d8`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0-18-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:9b6c71eab90311187fb40dc7addde1d9dc0624209e18bfff0b574bba8b226630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79442831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9901baf84d44edc45f517e508bd308d43a9c4eedc168ea3c29e56b23f5de2a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:30:59 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 07:51:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:51:06 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:51:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:51:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:51:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:51:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:25:30 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:25:30 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:25:30 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:25:31 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:26:03 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:26:05 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:26:05 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:26:05 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:26:05 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:26:05 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba3ec755ffa1858566fb0656750edff534b6ed03c9078392fb0c19cb10b4f8d`  
		Last Modified: Sat, 16 Mar 2024 08:14:10 GMT  
		Size: 39.8 MB (39816343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dafbded8808a388313b6f83fb3ee6df3ba8ce31c7ba159dd5f660e2dde30581`  
		Last Modified: Sat, 16 Mar 2024 08:14:06 GMT  
		Size: 2.3 MB (2342589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4f9a3ef664bbf378ffcb5942bc44e7cd5e6b4d1c688cf44065e731fb903cb`  
		Last Modified: Sat, 16 Mar 2024 08:14:05 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fccb851668e56077568c2412f62d9dd8c4bd945c763e023e072acb7417630c0`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd1b4af91499eb4e0213faff62b10ae12243e4c43dd5bd5010bfa50cb65b20c`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d5141fd23193bb9201e4bd3cc5093b0fb10b1e2a2c0cc4c637b71db2fc6f3d`  
		Last Modified: Sat, 16 Mar 2024 13:27:23 GMT  
		Size: 33.1 MB (33062121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd0bcf46415de040e9ec87d689f9379e65d9049a254fa2f5a50f3a1dbb8bc5b`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0-18-alpine3.19`

```console
$ docker pull mongo-express@sha256:9bbefb7db134c3fa06ffb90577316f73c1a1e9f0387280fe1bea437c5e47a92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0-18-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:293b21d1c1ca95a54eceba59f263161b0e642cbd72b57cc3c7cc3208b8ae259b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79847087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9232c24c4474e63f71c115ca7eae2b2273681845bf5bd34c4b5eb148c4dcc5d`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:31:48 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 03:31:56 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:57 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:32:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:32:02 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:32:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:32:02 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:50:45 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:50:45 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:50:45 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:50:45 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:51:22 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:51:24 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:51:24 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:51:24 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:51:24 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:51:24 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff171c16ee4e8ed3a0ae3edb6fb9558f281134a3879eedca7d79fc2e16e46073`  
		Last Modified: Sat, 16 Mar 2024 03:35:45 GMT  
		Size: 40.2 MB (40246754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c215e7ef3945bd4fdac5a20f1e4a29c62f28c8493ad05d3e651d62cf069140d`  
		Last Modified: Sat, 16 Mar 2024 03:35:39 GMT  
		Size: 2.3 MB (2342788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f72a72846173b6a02c1f73db9a74aca2af50fb39bf13ba2e4d12d13e5722d6c`  
		Last Modified: Sat, 16 Mar 2024 03:35:38 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5fc007d83ce2bea3e3e3e15b08c1941c5e7c244261d06bcf4f749c27679f2b`  
		Last Modified: Sat, 16 Mar 2024 12:53:17 GMT  
		Size: 784.7 KB (784714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dc20ed69fe2ba1321f8b6ca6be9ffa8256f6fa567d80f8a1fab80635ac6b9b`  
		Last Modified: Sat, 16 Mar 2024 12:53:17 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bed48b4f41b43763eb67104ba454968a725631dfcd68ffe875cf0aed2ed9b8e`  
		Last Modified: Sat, 16 Mar 2024 12:53:25 GMT  
		Size: 33.1 MB (33062676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8815f593fde212d510e4eb025d8f4f62b0a22a73e95ea68e7b31c1c8aeddde89`  
		Last Modified: Sat, 16 Mar 2024 12:53:17 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0-18-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:c0a6f6cc78eb16fdec4e25ce052ddf728f400dec8727bbd0c3fa5d6ca555de36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79616499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64f825c616364113e155c323b65b3aeac7654b0ebe20f99831d9f07e4025b11`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:51:22 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 08:11:07 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 08:11:07 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 08:11:12 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 08:11:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 08:11:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:11:12 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:24:50 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:24:50 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:24:50 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:24:51 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:25:23 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:25:25 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:25:25 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:25:25 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:25:25 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:25:25 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8657c71df119fa73d920b9e13c4d78e0b9c1ebcd073c3aec39cf36438d61231`  
		Last Modified: Sat, 16 Mar 2024 08:14:25 GMT  
		Size: 40.0 MB (39999911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048cf8cd15c8c1bdbd097e3168104729b5bdcffd2bbcd63b0124860f4fff0c21`  
		Last Modified: Sat, 16 Mar 2024 08:14:21 GMT  
		Size: 2.3 MB (2342746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ee200833ea33ad51efcd618903682b620e0d2cd420bc015a9c0a69ddc12a9e`  
		Last Modified: Sat, 16 Mar 2024 08:14:21 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c293927a519eba54163565007446d5418cbae0dcc7476b3d4a69e059e6a4406c`  
		Last Modified: Sat, 16 Mar 2024 13:27:01 GMT  
		Size: 862.4 KB (862436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c91c830721fda0245fc134f9d0b897126b7d854deead137939577abd8891640`  
		Last Modified: Sat, 16 Mar 2024 13:27:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a314aeac73211adfc52cd132c20b7861c8dee5d03d5ae441f8eea66d25605414`  
		Last Modified: Sat, 16 Mar 2024 13:27:07 GMT  
		Size: 33.1 MB (33062265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac137ed14914e03f924e95670d9be81b750765cb2d966d5188faee97982f14e`  
		Last Modified: Sat, 16 Mar 2024 13:27:01 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0-20`

```console
$ docker pull mongo-express@sha256:e621529902f686e864594a6db9948a64c4b022b3481c6ae2ec1f423f05eff15a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0-20` - linux; amd64

```console
$ docker pull mongo-express@sha256:ca06869055714bd880af47ebcba4345440b613605dcf463dd2375d909ca375f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81670554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef18415bc705b4e9e137f80183aebcd70d309715c710683aa28e74ecb6f4a66`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:30:36 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 03:30:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:30:46 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:30:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:30:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:30:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:30:51 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:49:56 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:49:56 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:49:56 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:49:56 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:50:33 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:50:34 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:50:34 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:50:34 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:50:34 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:50:35 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2a61871030542f55a6ec81ca7e2b393c7e3392e58a1fd97e5edfacd89918e2`  
		Last Modified: Sat, 16 Mar 2024 03:34:28 GMT  
		Size: 42.1 MB (42061773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243431d75724ed545c16e7216326878fbd58e429991be8dcca467107d144517`  
		Last Modified: Sat, 16 Mar 2024 03:34:22 GMT  
		Size: 2.3 MB (2341048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f042e74e78671927ad1a1d4ac10d69571054a09d0bce420d39ac4b857222a19`  
		Last Modified: Sat, 16 Mar 2024 03:34:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a4b4df73f1495ffa0079e4cd4ae221f2e13a9a0c676f1275d435b6e1aa7e10`  
		Last Modified: Sat, 16 Mar 2024 12:52:54 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a98bdbbeb961d54e068e47479f01ad7242d8eeb7d761f0fab69385695ec84d9`  
		Last Modified: Sat, 16 Mar 2024 12:52:53 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359f92ee7dd2c9e9f8d84548d57fbd10d0b29726e11f09c4dd34a575042f8732`  
		Last Modified: Sat, 16 Mar 2024 12:53:01 GMT  
		Size: 33.1 MB (33061447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c029ea17cdba5d5ac5448578edc7846dfdad17ab63c7a8844d6bcdc413ba98`  
		Last Modified: Sat, 16 Mar 2024 12:52:53 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0-20` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:01c3e3290cb8c4bf17bf766191d955a3b7c841ea5fe9cc4fa2878739e1be112a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81436380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236929dda6d6ad438b42a02149357f015f469d9a7009f3dc0e8582c501ded5ba`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:43:17 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 07:07:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:07:05 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:07:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:07:10 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:07:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:07:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:24:10 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:24:10 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:24:10 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:24:10 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:24:42 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:24:44 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:24:44 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:24:44 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:24:45 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:24:45 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014cc7646ef4d291a260436dd0c6949d8be2d31a1d562074b83222be1fc67c00`  
		Last Modified: Sat, 16 Mar 2024 08:13:13 GMT  
		Size: 41.8 MB (41812067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70242eaeabbd114d411d9a4e028012cf5a6603cbdcd6071c9a3cf98c712f01f`  
		Last Modified: Sat, 16 Mar 2024 08:13:09 GMT  
		Size: 2.3 MB (2340908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c48c4eabd9390f8a6b50d058cd1d4f09b299fa3d9e42a248c938b71c72c9212`  
		Last Modified: Sat, 16 Mar 2024 08:13:08 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047c003e3455e0498efd76e3b414efa7b3ee9dba486c3bca18f526b8e5475134`  
		Last Modified: Sat, 16 Mar 2024 13:26:39 GMT  
		Size: 887.0 KB (887003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dda267073c82524fa9a9b1ea5b8557db6e7b63f88a6d972b218ce9ac15138b`  
		Last Modified: Sat, 16 Mar 2024 13:26:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890347fa336e7376ea17ad33e269afe68b46193df94b4056440c70f6a92f17cb`  
		Last Modified: Sat, 16 Mar 2024 13:26:45 GMT  
		Size: 33.1 MB (33061618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a28b2b96503114222dfb0726756b780751497362797c05e8b56d3ff8e3701d`  
		Last Modified: Sat, 16 Mar 2024 13:26:38 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0-20-alpine3.18`

```console
$ docker pull mongo-express@sha256:e621529902f686e864594a6db9948a64c4b022b3481c6ae2ec1f423f05eff15a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0-20-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:ca06869055714bd880af47ebcba4345440b613605dcf463dd2375d909ca375f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81670554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef18415bc705b4e9e137f80183aebcd70d309715c710683aa28e74ecb6f4a66`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:30:36 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 03:30:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:30:46 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:30:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:30:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:30:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:30:51 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:49:56 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:49:56 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:49:56 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:49:56 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:50:33 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:50:34 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:50:34 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:50:34 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:50:34 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:50:35 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2a61871030542f55a6ec81ca7e2b393c7e3392e58a1fd97e5edfacd89918e2`  
		Last Modified: Sat, 16 Mar 2024 03:34:28 GMT  
		Size: 42.1 MB (42061773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243431d75724ed545c16e7216326878fbd58e429991be8dcca467107d144517`  
		Last Modified: Sat, 16 Mar 2024 03:34:22 GMT  
		Size: 2.3 MB (2341048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f042e74e78671927ad1a1d4ac10d69571054a09d0bce420d39ac4b857222a19`  
		Last Modified: Sat, 16 Mar 2024 03:34:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a4b4df73f1495ffa0079e4cd4ae221f2e13a9a0c676f1275d435b6e1aa7e10`  
		Last Modified: Sat, 16 Mar 2024 12:52:54 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a98bdbbeb961d54e068e47479f01ad7242d8eeb7d761f0fab69385695ec84d9`  
		Last Modified: Sat, 16 Mar 2024 12:52:53 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359f92ee7dd2c9e9f8d84548d57fbd10d0b29726e11f09c4dd34a575042f8732`  
		Last Modified: Sat, 16 Mar 2024 12:53:01 GMT  
		Size: 33.1 MB (33061447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c029ea17cdba5d5ac5448578edc7846dfdad17ab63c7a8844d6bcdc413ba98`  
		Last Modified: Sat, 16 Mar 2024 12:52:53 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0-20-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:01c3e3290cb8c4bf17bf766191d955a3b7c841ea5fe9cc4fa2878739e1be112a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81436380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236929dda6d6ad438b42a02149357f015f469d9a7009f3dc0e8582c501ded5ba`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:43:17 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 07:07:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:07:05 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:07:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:07:10 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:07:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:07:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:24:10 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:24:10 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:24:10 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:24:10 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:24:42 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:24:44 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:24:44 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:24:44 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:24:45 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:24:45 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014cc7646ef4d291a260436dd0c6949d8be2d31a1d562074b83222be1fc67c00`  
		Last Modified: Sat, 16 Mar 2024 08:13:13 GMT  
		Size: 41.8 MB (41812067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70242eaeabbd114d411d9a4e028012cf5a6603cbdcd6071c9a3cf98c712f01f`  
		Last Modified: Sat, 16 Mar 2024 08:13:09 GMT  
		Size: 2.3 MB (2340908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c48c4eabd9390f8a6b50d058cd1d4f09b299fa3d9e42a248c938b71c72c9212`  
		Last Modified: Sat, 16 Mar 2024 08:13:08 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047c003e3455e0498efd76e3b414efa7b3ee9dba486c3bca18f526b8e5475134`  
		Last Modified: Sat, 16 Mar 2024 13:26:39 GMT  
		Size: 887.0 KB (887003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dda267073c82524fa9a9b1ea5b8557db6e7b63f88a6d972b218ce9ac15138b`  
		Last Modified: Sat, 16 Mar 2024 13:26:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890347fa336e7376ea17ad33e269afe68b46193df94b4056440c70f6a92f17cb`  
		Last Modified: Sat, 16 Mar 2024 13:26:45 GMT  
		Size: 33.1 MB (33061618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a28b2b96503114222dfb0726756b780751497362797c05e8b56d3ff8e3701d`  
		Last Modified: Sat, 16 Mar 2024 13:26:38 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0-20-alpine3.19`

```console
$ docker pull mongo-express@sha256:64c3652d3d858bc670a6d6f4e1dcf372743d99286342581f84c79bd64aebd1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0-20-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:e51caebda20038d36a0a927945ac46982937830885d61f8365ff7f87da39c937
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81784162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e700d78696bd1f925f9ccf20b1570d85e2f237cb31d7d0f82d4313a14ed4c7`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:30:54 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 03:31:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:03 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:31:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:31:09 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:31:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:31:09 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:49:07 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:49:07 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:49:07 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:49:07 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:49:44 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:49:45 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:49:45 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:49:45 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:49:45 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:49:45 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f16480e2ff54481cb1ea1553429bf399e8269985ab0dec5b5af6f55ea747d3f`  
		Last Modified: Sat, 16 Mar 2024 03:34:48 GMT  
		Size: 42.2 MB (42186770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092226d52cac3f544d7973fe7ba4416bc2cd5b69e4016804efb95026fe6b108b`  
		Last Modified: Sat, 16 Mar 2024 03:34:41 GMT  
		Size: 2.3 MB (2341056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0493dfb2ff9c5bd770291dc14d4e30caff25c72bcdfbea04e9bf2f4013e21db0`  
		Last Modified: Sat, 16 Mar 2024 03:34:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ecd5787d8d96f063e89ed863d50acf522cf19bc960893428920be3e3f403e4`  
		Last Modified: Sat, 16 Mar 2024 12:52:36 GMT  
		Size: 784.7 KB (784709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef3edd5aece8b5458b4fec1593302b5d5a5f8e817968506db7dc59199097b0`  
		Last Modified: Sat, 16 Mar 2024 12:52:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852a8f6e0ae3bd255b309479997ea09526d64229d82dd929ff007dc63b397de0`  
		Last Modified: Sat, 16 Mar 2024 12:52:43 GMT  
		Size: 33.1 MB (33061473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beea5e3312ccc3a4a79efc11323b1946692f97158ba5c7f1a58fbd1b0d25947`  
		Last Modified: Sat, 16 Mar 2024 12:52:36 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0-20-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:eced3cdd6dcb4339b1255ece128faab3277ca31df13d139d8a3a6b16d9345477
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81627062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc62706911d7e3947b710307426dacfb496cdfe495e665a7e0376a39dc94e268`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:07:25 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 07:30:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:30:31 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:30:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:30:35 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:30:36 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:23:22 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:23:22 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:23:22 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:23:22 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:23:59 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:24:01 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:24:01 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:24:01 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:24:01 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:24:01 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93210f2a425301d4d76217e169b2005256fefe022ef4181715a590880a055162`  
		Last Modified: Sat, 16 Mar 2024 08:13:30 GMT  
		Size: 42.0 MB (42013649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef1c9a74cd88ae4dee8daee6d9a39425cb8411294789b3118317c9acc154648`  
		Last Modified: Sat, 16 Mar 2024 08:13:25 GMT  
		Size: 2.3 MB (2340967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bb1a28a290af7381f606e1a4492f0163ccbd60ee0daf41b43ffa0dd7d98676`  
		Last Modified: Sat, 16 Mar 2024 08:13:25 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1af0335e763361bf72725ef483ea81cc489a55273d74f649d71259497d7cbf`  
		Last Modified: Sat, 16 Mar 2024 13:26:22 GMT  
		Size: 862.4 KB (862443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449cfdb74fb98eb2a47fc6dd00edcc8959fcc9bf43c9b105dd6ad94513fc482d`  
		Last Modified: Sat, 16 Mar 2024 13:26:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0649943d1a66d3de1075fa69074fbba9f2984d6d9764a4c8dfaa0da83f9ec5`  
		Last Modified: Sat, 16 Mar 2024 13:26:28 GMT  
		Size: 33.1 MB (33060866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640ffa86d7bde36df864b1c5fb89700124947dfb5388a8d6e50f61701e47e1b6`  
		Last Modified: Sat, 16 Mar 2024 13:26:22 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.2`

```console
$ docker pull mongo-express@sha256:66dfa6a39deffce1935669807d205eca3edd7a8459c701ffe75d7e3e81df10ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.2` - linux; amd64

```console
$ docker pull mongo-express@sha256:7350263cc85ce61aee73dac649094ebbdb3312e72d7b8730ad6dd4fecf52c8cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79723055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3c796960930a5f7ca3e7f324513a1d17f244fac1fe6b43f401385b7a4dcd9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:31:30 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 03:31:39 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:39 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:31:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:31:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:31:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:31:44 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:51:34 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:51:34 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:51:34 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:51:35 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:52:12 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:52:13 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:52:13 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:52:13 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:52:14 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:52:14 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bbeb28556ec2281a75a0dd28eac89ea4e8061f158b8d46fbd152a65d941a45`  
		Last Modified: Sat, 16 Mar 2024 03:35:27 GMT  
		Size: 40.1 MB (40110896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c579a9bd17009e90ba555dd059d4888d47caba34c05aa588d1be8eb99be497a4`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 2.3 MB (2342667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745a187ebdeee71b739cc7f33b1ed13c1e1721e22582bfef4056e8d16079a1f0`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f3c466a5e17fe5795a69aa5d28fea1309438865e867612227cdcf4e37546cd`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d198b3ae6a7adbe6be3f69aaeec427b4a3606ef39536b2cc08b4bd61260360`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba939722952f2a818595b15a63a2c30f0c524d72d96405589b812d1df53667c`  
		Last Modified: Sat, 16 Mar 2024 12:53:42 GMT  
		Size: 33.1 MB (33063206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc31ad8151e1f2e180ff57a1787d64518a0fe2cd8c27e78449dffba372cd40d8`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.2` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:9b6c71eab90311187fb40dc7addde1d9dc0624209e18bfff0b574bba8b226630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79442831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9901baf84d44edc45f517e508bd308d43a9c4eedc168ea3c29e56b23f5de2a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:30:59 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 07:51:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:51:06 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:51:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:51:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:51:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:51:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:25:30 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:25:30 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:25:30 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:25:31 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:26:03 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:26:05 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:26:05 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:26:05 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:26:05 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:26:05 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba3ec755ffa1858566fb0656750edff534b6ed03c9078392fb0c19cb10b4f8d`  
		Last Modified: Sat, 16 Mar 2024 08:14:10 GMT  
		Size: 39.8 MB (39816343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dafbded8808a388313b6f83fb3ee6df3ba8ce31c7ba159dd5f660e2dde30581`  
		Last Modified: Sat, 16 Mar 2024 08:14:06 GMT  
		Size: 2.3 MB (2342589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4f9a3ef664bbf378ffcb5942bc44e7cd5e6b4d1c688cf44065e731fb903cb`  
		Last Modified: Sat, 16 Mar 2024 08:14:05 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fccb851668e56077568c2412f62d9dd8c4bd945c763e023e072acb7417630c0`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd1b4af91499eb4e0213faff62b10ae12243e4c43dd5bd5010bfa50cb65b20c`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d5141fd23193bb9201e4bd3cc5093b0fb10b1e2a2c0cc4c637b71db2fc6f3d`  
		Last Modified: Sat, 16 Mar 2024 13:27:23 GMT  
		Size: 33.1 MB (33062121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd0bcf46415de040e9ec87d689f9379e65d9049a254fa2f5a50f3a1dbb8bc5b`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.2-18`

```console
$ docker pull mongo-express@sha256:66dfa6a39deffce1935669807d205eca3edd7a8459c701ffe75d7e3e81df10ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.2-18` - linux; amd64

```console
$ docker pull mongo-express@sha256:7350263cc85ce61aee73dac649094ebbdb3312e72d7b8730ad6dd4fecf52c8cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79723055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3c796960930a5f7ca3e7f324513a1d17f244fac1fe6b43f401385b7a4dcd9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:31:30 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 03:31:39 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:39 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:31:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:31:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:31:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:31:44 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:51:34 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:51:34 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:51:34 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:51:35 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:52:12 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:52:13 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:52:13 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:52:13 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:52:14 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:52:14 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bbeb28556ec2281a75a0dd28eac89ea4e8061f158b8d46fbd152a65d941a45`  
		Last Modified: Sat, 16 Mar 2024 03:35:27 GMT  
		Size: 40.1 MB (40110896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c579a9bd17009e90ba555dd059d4888d47caba34c05aa588d1be8eb99be497a4`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 2.3 MB (2342667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745a187ebdeee71b739cc7f33b1ed13c1e1721e22582bfef4056e8d16079a1f0`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f3c466a5e17fe5795a69aa5d28fea1309438865e867612227cdcf4e37546cd`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d198b3ae6a7adbe6be3f69aaeec427b4a3606ef39536b2cc08b4bd61260360`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba939722952f2a818595b15a63a2c30f0c524d72d96405589b812d1df53667c`  
		Last Modified: Sat, 16 Mar 2024 12:53:42 GMT  
		Size: 33.1 MB (33063206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc31ad8151e1f2e180ff57a1787d64518a0fe2cd8c27e78449dffba372cd40d8`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.2-18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:9b6c71eab90311187fb40dc7addde1d9dc0624209e18bfff0b574bba8b226630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79442831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9901baf84d44edc45f517e508bd308d43a9c4eedc168ea3c29e56b23f5de2a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:30:59 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 07:51:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:51:06 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:51:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:51:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:51:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:51:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:25:30 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:25:30 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:25:30 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:25:31 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:26:03 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:26:05 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:26:05 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:26:05 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:26:05 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:26:05 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba3ec755ffa1858566fb0656750edff534b6ed03c9078392fb0c19cb10b4f8d`  
		Last Modified: Sat, 16 Mar 2024 08:14:10 GMT  
		Size: 39.8 MB (39816343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dafbded8808a388313b6f83fb3ee6df3ba8ce31c7ba159dd5f660e2dde30581`  
		Last Modified: Sat, 16 Mar 2024 08:14:06 GMT  
		Size: 2.3 MB (2342589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4f9a3ef664bbf378ffcb5942bc44e7cd5e6b4d1c688cf44065e731fb903cb`  
		Last Modified: Sat, 16 Mar 2024 08:14:05 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fccb851668e56077568c2412f62d9dd8c4bd945c763e023e072acb7417630c0`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd1b4af91499eb4e0213faff62b10ae12243e4c43dd5bd5010bfa50cb65b20c`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d5141fd23193bb9201e4bd3cc5093b0fb10b1e2a2c0cc4c637b71db2fc6f3d`  
		Last Modified: Sat, 16 Mar 2024 13:27:23 GMT  
		Size: 33.1 MB (33062121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd0bcf46415de040e9ec87d689f9379e65d9049a254fa2f5a50f3a1dbb8bc5b`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.2-18-alpine3.18`

```console
$ docker pull mongo-express@sha256:66dfa6a39deffce1935669807d205eca3edd7a8459c701ffe75d7e3e81df10ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.2-18-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:7350263cc85ce61aee73dac649094ebbdb3312e72d7b8730ad6dd4fecf52c8cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79723055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3c796960930a5f7ca3e7f324513a1d17f244fac1fe6b43f401385b7a4dcd9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:31:30 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 03:31:39 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:39 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:31:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:31:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:31:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:31:44 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:51:34 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:51:34 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:51:34 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:51:35 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:52:12 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:52:13 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:52:13 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:52:13 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:52:14 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:52:14 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bbeb28556ec2281a75a0dd28eac89ea4e8061f158b8d46fbd152a65d941a45`  
		Last Modified: Sat, 16 Mar 2024 03:35:27 GMT  
		Size: 40.1 MB (40110896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c579a9bd17009e90ba555dd059d4888d47caba34c05aa588d1be8eb99be497a4`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 2.3 MB (2342667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745a187ebdeee71b739cc7f33b1ed13c1e1721e22582bfef4056e8d16079a1f0`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f3c466a5e17fe5795a69aa5d28fea1309438865e867612227cdcf4e37546cd`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d198b3ae6a7adbe6be3f69aaeec427b4a3606ef39536b2cc08b4bd61260360`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba939722952f2a818595b15a63a2c30f0c524d72d96405589b812d1df53667c`  
		Last Modified: Sat, 16 Mar 2024 12:53:42 GMT  
		Size: 33.1 MB (33063206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc31ad8151e1f2e180ff57a1787d64518a0fe2cd8c27e78449dffba372cd40d8`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.2-18-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:9b6c71eab90311187fb40dc7addde1d9dc0624209e18bfff0b574bba8b226630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79442831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9901baf84d44edc45f517e508bd308d43a9c4eedc168ea3c29e56b23f5de2a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:30:59 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 07:51:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:51:06 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:51:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:51:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:51:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:51:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:25:30 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:25:30 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:25:30 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:25:31 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:26:03 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:26:05 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:26:05 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:26:05 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:26:05 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:26:05 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba3ec755ffa1858566fb0656750edff534b6ed03c9078392fb0c19cb10b4f8d`  
		Last Modified: Sat, 16 Mar 2024 08:14:10 GMT  
		Size: 39.8 MB (39816343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dafbded8808a388313b6f83fb3ee6df3ba8ce31c7ba159dd5f660e2dde30581`  
		Last Modified: Sat, 16 Mar 2024 08:14:06 GMT  
		Size: 2.3 MB (2342589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4f9a3ef664bbf378ffcb5942bc44e7cd5e6b4d1c688cf44065e731fb903cb`  
		Last Modified: Sat, 16 Mar 2024 08:14:05 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fccb851668e56077568c2412f62d9dd8c4bd945c763e023e072acb7417630c0`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd1b4af91499eb4e0213faff62b10ae12243e4c43dd5bd5010bfa50cb65b20c`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d5141fd23193bb9201e4bd3cc5093b0fb10b1e2a2c0cc4c637b71db2fc6f3d`  
		Last Modified: Sat, 16 Mar 2024 13:27:23 GMT  
		Size: 33.1 MB (33062121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd0bcf46415de040e9ec87d689f9379e65d9049a254fa2f5a50f3a1dbb8bc5b`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.2-18-alpine3.19`

```console
$ docker pull mongo-express@sha256:9bbefb7db134c3fa06ffb90577316f73c1a1e9f0387280fe1bea437c5e47a92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.2-18-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:293b21d1c1ca95a54eceba59f263161b0e642cbd72b57cc3c7cc3208b8ae259b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79847087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9232c24c4474e63f71c115ca7eae2b2273681845bf5bd34c4b5eb148c4dcc5d`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:31:48 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 03:31:56 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:57 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:32:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:32:02 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:32:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:32:02 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:50:45 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:50:45 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:50:45 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:50:45 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:51:22 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:51:24 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:51:24 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:51:24 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:51:24 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:51:24 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff171c16ee4e8ed3a0ae3edb6fb9558f281134a3879eedca7d79fc2e16e46073`  
		Last Modified: Sat, 16 Mar 2024 03:35:45 GMT  
		Size: 40.2 MB (40246754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c215e7ef3945bd4fdac5a20f1e4a29c62f28c8493ad05d3e651d62cf069140d`  
		Last Modified: Sat, 16 Mar 2024 03:35:39 GMT  
		Size: 2.3 MB (2342788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f72a72846173b6a02c1f73db9a74aca2af50fb39bf13ba2e4d12d13e5722d6c`  
		Last Modified: Sat, 16 Mar 2024 03:35:38 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5fc007d83ce2bea3e3e3e15b08c1941c5e7c244261d06bcf4f749c27679f2b`  
		Last Modified: Sat, 16 Mar 2024 12:53:17 GMT  
		Size: 784.7 KB (784714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dc20ed69fe2ba1321f8b6ca6be9ffa8256f6fa567d80f8a1fab80635ac6b9b`  
		Last Modified: Sat, 16 Mar 2024 12:53:17 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bed48b4f41b43763eb67104ba454968a725631dfcd68ffe875cf0aed2ed9b8e`  
		Last Modified: Sat, 16 Mar 2024 12:53:25 GMT  
		Size: 33.1 MB (33062676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8815f593fde212d510e4eb025d8f4f62b0a22a73e95ea68e7b31c1c8aeddde89`  
		Last Modified: Sat, 16 Mar 2024 12:53:17 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.2-18-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:c0a6f6cc78eb16fdec4e25ce052ddf728f400dec8727bbd0c3fa5d6ca555de36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79616499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64f825c616364113e155c323b65b3aeac7654b0ebe20f99831d9f07e4025b11`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:51:22 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 08:11:07 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 08:11:07 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 08:11:12 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 08:11:12 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 08:11:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:11:12 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:24:50 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:24:50 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:24:50 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:24:51 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:25:23 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:25:25 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:25:25 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:25:25 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:25:25 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:25:25 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8657c71df119fa73d920b9e13c4d78e0b9c1ebcd073c3aec39cf36438d61231`  
		Last Modified: Sat, 16 Mar 2024 08:14:25 GMT  
		Size: 40.0 MB (39999911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048cf8cd15c8c1bdbd097e3168104729b5bdcffd2bbcd63b0124860f4fff0c21`  
		Last Modified: Sat, 16 Mar 2024 08:14:21 GMT  
		Size: 2.3 MB (2342746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ee200833ea33ad51efcd618903682b620e0d2cd420bc015a9c0a69ddc12a9e`  
		Last Modified: Sat, 16 Mar 2024 08:14:21 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c293927a519eba54163565007446d5418cbae0dcc7476b3d4a69e059e6a4406c`  
		Last Modified: Sat, 16 Mar 2024 13:27:01 GMT  
		Size: 862.4 KB (862436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c91c830721fda0245fc134f9d0b897126b7d854deead137939577abd8891640`  
		Last Modified: Sat, 16 Mar 2024 13:27:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a314aeac73211adfc52cd132c20b7861c8dee5d03d5ae441f8eea66d25605414`  
		Last Modified: Sat, 16 Mar 2024 13:27:07 GMT  
		Size: 33.1 MB (33062265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac137ed14914e03f924e95670d9be81b750765cb2d966d5188faee97982f14e`  
		Last Modified: Sat, 16 Mar 2024 13:27:01 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.2-20`

```console
$ docker pull mongo-express@sha256:e621529902f686e864594a6db9948a64c4b022b3481c6ae2ec1f423f05eff15a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.2-20` - linux; amd64

```console
$ docker pull mongo-express@sha256:ca06869055714bd880af47ebcba4345440b613605dcf463dd2375d909ca375f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81670554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef18415bc705b4e9e137f80183aebcd70d309715c710683aa28e74ecb6f4a66`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:30:36 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 03:30:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:30:46 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:30:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:30:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:30:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:30:51 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:49:56 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:49:56 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:49:56 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:49:56 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:50:33 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:50:34 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:50:34 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:50:34 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:50:34 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:50:35 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2a61871030542f55a6ec81ca7e2b393c7e3392e58a1fd97e5edfacd89918e2`  
		Last Modified: Sat, 16 Mar 2024 03:34:28 GMT  
		Size: 42.1 MB (42061773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243431d75724ed545c16e7216326878fbd58e429991be8dcca467107d144517`  
		Last Modified: Sat, 16 Mar 2024 03:34:22 GMT  
		Size: 2.3 MB (2341048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f042e74e78671927ad1a1d4ac10d69571054a09d0bce420d39ac4b857222a19`  
		Last Modified: Sat, 16 Mar 2024 03:34:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a4b4df73f1495ffa0079e4cd4ae221f2e13a9a0c676f1275d435b6e1aa7e10`  
		Last Modified: Sat, 16 Mar 2024 12:52:54 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a98bdbbeb961d54e068e47479f01ad7242d8eeb7d761f0fab69385695ec84d9`  
		Last Modified: Sat, 16 Mar 2024 12:52:53 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359f92ee7dd2c9e9f8d84548d57fbd10d0b29726e11f09c4dd34a575042f8732`  
		Last Modified: Sat, 16 Mar 2024 12:53:01 GMT  
		Size: 33.1 MB (33061447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c029ea17cdba5d5ac5448578edc7846dfdad17ab63c7a8844d6bcdc413ba98`  
		Last Modified: Sat, 16 Mar 2024 12:52:53 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.2-20` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:01c3e3290cb8c4bf17bf766191d955a3b7c841ea5fe9cc4fa2878739e1be112a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81436380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236929dda6d6ad438b42a02149357f015f469d9a7009f3dc0e8582c501ded5ba`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:43:17 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 07:07:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:07:05 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:07:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:07:10 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:07:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:07:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:24:10 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:24:10 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:24:10 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:24:10 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:24:42 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:24:44 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:24:44 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:24:44 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:24:45 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:24:45 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014cc7646ef4d291a260436dd0c6949d8be2d31a1d562074b83222be1fc67c00`  
		Last Modified: Sat, 16 Mar 2024 08:13:13 GMT  
		Size: 41.8 MB (41812067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70242eaeabbd114d411d9a4e028012cf5a6603cbdcd6071c9a3cf98c712f01f`  
		Last Modified: Sat, 16 Mar 2024 08:13:09 GMT  
		Size: 2.3 MB (2340908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c48c4eabd9390f8a6b50d058cd1d4f09b299fa3d9e42a248c938b71c72c9212`  
		Last Modified: Sat, 16 Mar 2024 08:13:08 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047c003e3455e0498efd76e3b414efa7b3ee9dba486c3bca18f526b8e5475134`  
		Last Modified: Sat, 16 Mar 2024 13:26:39 GMT  
		Size: 887.0 KB (887003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dda267073c82524fa9a9b1ea5b8557db6e7b63f88a6d972b218ce9ac15138b`  
		Last Modified: Sat, 16 Mar 2024 13:26:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890347fa336e7376ea17ad33e269afe68b46193df94b4056440c70f6a92f17cb`  
		Last Modified: Sat, 16 Mar 2024 13:26:45 GMT  
		Size: 33.1 MB (33061618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a28b2b96503114222dfb0726756b780751497362797c05e8b56d3ff8e3701d`  
		Last Modified: Sat, 16 Mar 2024 13:26:38 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.2-20-alpine3.18`

```console
$ docker pull mongo-express@sha256:e621529902f686e864594a6db9948a64c4b022b3481c6ae2ec1f423f05eff15a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.2-20-alpine3.18` - linux; amd64

```console
$ docker pull mongo-express@sha256:ca06869055714bd880af47ebcba4345440b613605dcf463dd2375d909ca375f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81670554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef18415bc705b4e9e137f80183aebcd70d309715c710683aa28e74ecb6f4a66`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:30:36 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 03:30:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:30:46 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:30:50 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:30:51 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:30:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:30:51 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:49:56 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:49:56 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:49:56 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:49:56 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:50:33 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:50:34 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:50:34 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:50:34 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:50:34 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:50:35 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2a61871030542f55a6ec81ca7e2b393c7e3392e58a1fd97e5edfacd89918e2`  
		Last Modified: Sat, 16 Mar 2024 03:34:28 GMT  
		Size: 42.1 MB (42061773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243431d75724ed545c16e7216326878fbd58e429991be8dcca467107d144517`  
		Last Modified: Sat, 16 Mar 2024 03:34:22 GMT  
		Size: 2.3 MB (2341048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f042e74e78671927ad1a1d4ac10d69571054a09d0bce420d39ac4b857222a19`  
		Last Modified: Sat, 16 Mar 2024 03:34:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a4b4df73f1495ffa0079e4cd4ae221f2e13a9a0c676f1275d435b6e1aa7e10`  
		Last Modified: Sat, 16 Mar 2024 12:52:54 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a98bdbbeb961d54e068e47479f01ad7242d8eeb7d761f0fab69385695ec84d9`  
		Last Modified: Sat, 16 Mar 2024 12:52:53 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359f92ee7dd2c9e9f8d84548d57fbd10d0b29726e11f09c4dd34a575042f8732`  
		Last Modified: Sat, 16 Mar 2024 12:53:01 GMT  
		Size: 33.1 MB (33061447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c029ea17cdba5d5ac5448578edc7846dfdad17ab63c7a8844d6bcdc413ba98`  
		Last Modified: Sat, 16 Mar 2024 12:52:53 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.2-20-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:01c3e3290cb8c4bf17bf766191d955a3b7c841ea5fe9cc4fa2878739e1be112a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81436380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236929dda6d6ad438b42a02149357f015f469d9a7009f3dc0e8582c501ded5ba`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:43:17 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 07:07:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:07:05 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:07:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:07:10 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:07:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:07:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:24:10 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:24:10 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:24:10 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:24:10 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:24:42 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:24:44 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:24:44 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:24:44 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:24:45 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:24:45 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014cc7646ef4d291a260436dd0c6949d8be2d31a1d562074b83222be1fc67c00`  
		Last Modified: Sat, 16 Mar 2024 08:13:13 GMT  
		Size: 41.8 MB (41812067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70242eaeabbd114d411d9a4e028012cf5a6603cbdcd6071c9a3cf98c712f01f`  
		Last Modified: Sat, 16 Mar 2024 08:13:09 GMT  
		Size: 2.3 MB (2340908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c48c4eabd9390f8a6b50d058cd1d4f09b299fa3d9e42a248c938b71c72c9212`  
		Last Modified: Sat, 16 Mar 2024 08:13:08 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047c003e3455e0498efd76e3b414efa7b3ee9dba486c3bca18f526b8e5475134`  
		Last Modified: Sat, 16 Mar 2024 13:26:39 GMT  
		Size: 887.0 KB (887003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dda267073c82524fa9a9b1ea5b8557db6e7b63f88a6d972b218ce9ac15138b`  
		Last Modified: Sat, 16 Mar 2024 13:26:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890347fa336e7376ea17ad33e269afe68b46193df94b4056440c70f6a92f17cb`  
		Last Modified: Sat, 16 Mar 2024 13:26:45 GMT  
		Size: 33.1 MB (33061618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a28b2b96503114222dfb0726756b780751497362797c05e8b56d3ff8e3701d`  
		Last Modified: Sat, 16 Mar 2024 13:26:38 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:1.0.2-20-alpine3.19`

```console
$ docker pull mongo-express@sha256:64c3652d3d858bc670a6d6f4e1dcf372743d99286342581f84c79bd64aebd1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:1.0.2-20-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:e51caebda20038d36a0a927945ac46982937830885d61f8365ff7f87da39c937
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81784162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e700d78696bd1f925f9ccf20b1570d85e2f237cb31d7d0f82d4313a14ed4c7`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:30:54 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 03:31:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:03 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:31:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:31:09 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:31:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:31:09 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:49:07 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:49:07 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:49:07 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:49:07 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:49:44 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:49:45 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:49:45 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:49:45 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:49:45 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:49:45 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f16480e2ff54481cb1ea1553429bf399e8269985ab0dec5b5af6f55ea747d3f`  
		Last Modified: Sat, 16 Mar 2024 03:34:48 GMT  
		Size: 42.2 MB (42186770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092226d52cac3f544d7973fe7ba4416bc2cd5b69e4016804efb95026fe6b108b`  
		Last Modified: Sat, 16 Mar 2024 03:34:41 GMT  
		Size: 2.3 MB (2341056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0493dfb2ff9c5bd770291dc14d4e30caff25c72bcdfbea04e9bf2f4013e21db0`  
		Last Modified: Sat, 16 Mar 2024 03:34:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ecd5787d8d96f063e89ed863d50acf522cf19bc960893428920be3e3f403e4`  
		Last Modified: Sat, 16 Mar 2024 12:52:36 GMT  
		Size: 784.7 KB (784709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef3edd5aece8b5458b4fec1593302b5d5a5f8e817968506db7dc59199097b0`  
		Last Modified: Sat, 16 Mar 2024 12:52:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852a8f6e0ae3bd255b309479997ea09526d64229d82dd929ff007dc63b397de0`  
		Last Modified: Sat, 16 Mar 2024 12:52:43 GMT  
		Size: 33.1 MB (33061473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beea5e3312ccc3a4a79efc11323b1946692f97158ba5c7f1a58fbd1b0d25947`  
		Last Modified: Sat, 16 Mar 2024 12:52:36 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:1.0.2-20-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:eced3cdd6dcb4339b1255ece128faab3277ca31df13d139d8a3a6b16d9345477
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81627062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc62706911d7e3947b710307426dacfb496cdfe495e665a7e0376a39dc94e268`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:07:25 GMT
ENV NODE_VERSION=20.11.1
# Sat, 16 Mar 2024 07:30:30 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5da733c21c3b51193a4fe9fc5be6cfa9a694d13b8d766eb02dbe4b8996547050" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:30:31 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:30:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:30:35 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:30:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:30:36 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:23:22 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:23:22 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:23:22 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:23:22 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:23:59 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:24:01 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:24:01 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:24:01 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:24:01 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:24:01 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93210f2a425301d4d76217e169b2005256fefe022ef4181715a590880a055162`  
		Last Modified: Sat, 16 Mar 2024 08:13:30 GMT  
		Size: 42.0 MB (42013649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef1c9a74cd88ae4dee8daee6d9a39425cb8411294789b3118317c9acc154648`  
		Last Modified: Sat, 16 Mar 2024 08:13:25 GMT  
		Size: 2.3 MB (2340967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bb1a28a290af7381f606e1a4492f0163ccbd60ee0daf41b43ffa0dd7d98676`  
		Last Modified: Sat, 16 Mar 2024 08:13:25 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1af0335e763361bf72725ef483ea81cc489a55273d74f649d71259497d7cbf`  
		Last Modified: Sat, 16 Mar 2024 13:26:22 GMT  
		Size: 862.4 KB (862443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449cfdb74fb98eb2a47fc6dd00edcc8959fcc9bf43c9b105dd6ad94513fc482d`  
		Last Modified: Sat, 16 Mar 2024 13:26:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0649943d1a66d3de1075fa69074fbba9f2984d6d9764a4c8dfaa0da83f9ec5`  
		Last Modified: Sat, 16 Mar 2024 13:26:28 GMT  
		Size: 33.1 MB (33060866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640ffa86d7bde36df864b1c5fb89700124947dfb5388a8d6e50f61701e47e1b6`  
		Last Modified: Sat, 16 Mar 2024 13:26:22 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo-express:latest`

```console
$ docker pull mongo-express@sha256:66dfa6a39deffce1935669807d205eca3edd7a8459c701ffe75d7e3e81df10ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo-express:latest` - linux; amd64

```console
$ docker pull mongo-express@sha256:7350263cc85ce61aee73dac649094ebbdb3312e72d7b8730ad6dd4fecf52c8cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79723055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3c796960930a5f7ca3e7f324513a1d17f244fac1fe6b43f401385b7a4dcd9a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:31:30 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 03:31:39 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 03:31:39 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 03:31:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 03:31:44 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:31:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:31:44 GMT
CMD ["node"]
# Sat, 16 Mar 2024 12:51:34 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 12:51:34 GMT
WORKDIR /app
# Sat, 16 Mar 2024 12:51:34 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 12:51:35 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 12:52:12 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 12:52:13 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 12:52:13 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 12:52:13 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 12:52:14 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 12:52:14 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bbeb28556ec2281a75a0dd28eac89ea4e8061f158b8d46fbd152a65d941a45`  
		Last Modified: Sat, 16 Mar 2024 03:35:27 GMT  
		Size: 40.1 MB (40110896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c579a9bd17009e90ba555dd059d4888d47caba34c05aa588d1be8eb99be497a4`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 2.3 MB (2342667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745a187ebdeee71b739cc7f33b1ed13c1e1721e22582bfef4056e8d16079a1f0`  
		Last Modified: Sat, 16 Mar 2024 03:35:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f3c466a5e17fe5795a69aa5d28fea1309438865e867612227cdcf4e37546cd`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 802.3 KB (802320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d198b3ae6a7adbe6be3f69aaeec427b4a3606ef39536b2cc08b4bd61260360`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba939722952f2a818595b15a63a2c30f0c524d72d96405589b812d1df53667c`  
		Last Modified: Sat, 16 Mar 2024 12:53:42 GMT  
		Size: 33.1 MB (33063206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc31ad8151e1f2e180ff57a1787d64518a0fe2cd8c27e78449dffba372cd40d8`  
		Last Modified: Sat, 16 Mar 2024 12:53:35 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo-express:latest` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:9b6c71eab90311187fb40dc7addde1d9dc0624209e18bfff0b574bba8b226630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79442831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9901baf84d44edc45f517e508bd308d43a9c4eedc168ea3c29e56b23f5de2a`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:30:59 GMT
ENV NODE_VERSION=18.19.1
# Sat, 16 Mar 2024 07:51:06 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="847973e34c5a579f706d9ad536ad3e35209cf4eac14ef9b88a8c842fd063c9cb" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version
# Sat, 16 Mar 2024 07:51:06 GMT
ENV YARN_VERSION=1.22.19
# Sat, 16 Mar 2024 07:51:10 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version
# Sat, 16 Mar 2024 07:51:11 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:51:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:51:11 GMT
CMD ["node"]
# Sat, 16 Mar 2024 13:25:30 GMT
RUN set -eux;     apk add --no-cache         bash         tini
# Sat, 16 Mar 2024 13:25:30 GMT
WORKDIR /app
# Sat, 16 Mar 2024 13:25:30 GMT
ARG MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express
# Sat, 16 Mar 2024 13:25:31 GMT
ARG MONGO_EXPRESS_VERSION=release/v1.0.2
# Sat, 16 Mar 2024 13:26:03 GMT
# ARGS: MONGO_EXPRESS_REPOSITORY=mongo-express/mongo-express MONGO_EXPRESS_VERSION=release/v1.0.2
RUN set -eux;     apk add --no-cache --virtual .me-fetch-deps git;     git clone --depth 1 --branch "$MONGO_EXPRESS_VERSION" -c advice.detachedHead=false https://github.com/$MONGO_EXPRESS_REPOSITORY.git .;     export DISABLE_V8_COMPILE_CACHE=1;     yarn install;     yarn build;     apk del --no-network .me-fetch-deps;     rm -rf .git* ~/.cache ~/.yarn
# Sat, 16 Mar 2024 13:26:05 GMT
ENV ME_CONFIG_MONGODB_URL=mongodb://mongo:27017 ME_CONFIG_MONGODB_ENABLE_ADMIN=true ME_CONFIG_SITE_SESSIONSECRET=secret ME_CONFIG_BASICAUTH=true VCAP_APP_HOST=0.0.0.0
# Sat, 16 Mar 2024 13:26:05 GMT
EXPOSE 8081
# Sat, 16 Mar 2024 13:26:05 GMT
COPY file:1fbcb9f1d4f70587b6312cc26764f8d10153fb54e0c11534a87d1dac7043974d in / 
# Sat, 16 Mar 2024 13:26:05 GMT
ENTRYPOINT ["/sbin/tini" "--" "/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 13:26:05 GMT
CMD ["mongo-express"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba3ec755ffa1858566fb0656750edff534b6ed03c9078392fb0c19cb10b4f8d`  
		Last Modified: Sat, 16 Mar 2024 08:14:10 GMT  
		Size: 39.8 MB (39816343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dafbded8808a388313b6f83fb3ee6df3ba8ce31c7ba159dd5f660e2dde30581`  
		Last Modified: Sat, 16 Mar 2024 08:14:06 GMT  
		Size: 2.3 MB (2342589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4f9a3ef664bbf378ffcb5942bc44e7cd5e6b4d1c688cf44065e731fb903cb`  
		Last Modified: Sat, 16 Mar 2024 08:14:05 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fccb851668e56077568c2412f62d9dd8c4bd945c763e023e072acb7417630c0`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 887.0 KB (886994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd1b4af91499eb4e0213faff62b10ae12243e4c43dd5bd5010bfa50cb65b20c`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d5141fd23193bb9201e4bd3cc5093b0fb10b1e2a2c0cc4c637b71db2fc6f3d`  
		Last Modified: Sat, 16 Mar 2024 13:27:23 GMT  
		Size: 33.1 MB (33062121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd0bcf46415de040e9ec87d689f9379e65d9049a254fa2f5a50f3a1dbb8bc5b`  
		Last Modified: Sat, 16 Mar 2024 13:27:17 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

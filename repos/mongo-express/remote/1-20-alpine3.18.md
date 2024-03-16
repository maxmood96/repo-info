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

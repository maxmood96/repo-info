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

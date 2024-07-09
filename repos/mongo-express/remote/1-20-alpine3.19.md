## `mongo-express:1-20-alpine3.19`

```console
$ docker pull mongo-express@sha256:31f2dbd3c4eda00dd442a3f1331c2dfce576fc99ebc06cf13900586659cab499
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1-20-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:e9208abccd8c02a6f97872b9b199fa948f1769994f0a2c07a92ef235670c58aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61423826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728f79acad2b31fa9295038c4760f311f86a83901914c09deb066b41014030d4`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
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
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2eced66f694533e87a42cacdeb282e85ab86e92ef668272f080e974f3f7c9b`  
		Last Modified: Tue, 09 Jul 2024 16:49:38 GMT  
		Size: 42.2 MB (42192990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6691bc11971463d3567129cbfbb7037d038f631830d21aeb9c21b50360a1d46b`  
		Last Modified: Tue, 09 Jul 2024 16:49:38 GMT  
		Size: 1.4 MB (1387223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79202f6f56b470cbb8ba8e25d4fe197f3db201d13d813785a33b35c3d632693f`  
		Last Modified: Tue, 09 Jul 2024 16:49:38 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9485ace0fa17f6becd45f003941cb533c7095c6ade80f5ebacf4dee8123ebef`  
		Last Modified: Tue, 09 Jul 2024 17:50:30 GMT  
		Size: 784.7 KB (784652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c69035126ab053a736a8d3f54aaeafc84e9d6299815384dd912ad6a4acf0b78`  
		Last Modified: Tue, 09 Jul 2024 17:50:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba4a80e090a805cbdf211104f213968565ea2f54ec8b75e11d9557ae7158d7b`  
		Last Modified: Tue, 09 Jul 2024 17:50:30 GMT  
		Size: 13.6 MB (13640237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6118c0c226ca34fb1568c72caf7e228ed351c8da49056b82a34164992f40efbd`  
		Last Modified: Tue, 09 Jul 2024 17:50:30 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-20-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:a4d69a2af6f6465591779df4f5e502797e9c58d37b7eddadc040737c4159aad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.4 KB (867355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0617dcc675e1720875c4ffa971ddd66c98aec6017cf920f29e08a31286bf3998`

```dockerfile
```

-	Layers:
	-	`sha256:7b042db88cf341218b5f5add3a124f273dcc27e1e22d8ac2f9d1e9bfea4c72b9`  
		Last Modified: Tue, 09 Jul 2024 17:50:30 GMT  
		Size: 852.1 KB (852091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe004d730438dec5ac9785f62c6c44e8b6c30b35850d29400f070f34160012b`  
		Last Modified: Tue, 09 Jul 2024 17:50:30 GMT  
		Size: 15.3 KB (15264 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1-20-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:5e054f77d4259cc22325f136ec6cc769da7c3c5e244ebe6def6406d8675b5b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61253145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1c8baf88963b18a5e6885369d5531a1eb850a50b09347d07576a563dd44444`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=20.15.0
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="24a21bc2fd2caf300ea36d716fbfa29ababa8a41bb844e67b6cf8b3d5091792c" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
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
	-	`sha256:b47753cedc39a77655573df122e09070e12281b182d8c4554714b608c1c40461`  
		Last Modified: Mon, 24 Jun 2024 22:18:59 GMT  
		Size: 42.0 MB (42004602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3b7bd7d5fc56a91b622bdcef788eca9345b7d94a36600f0e3f6b79e63fec3c`  
		Last Modified: Mon, 24 Jun 2024 22:18:58 GMT  
		Size: 1.4 MB (1387218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f947ce7c424895a438ada3c1bd2b8860d9b916ce229fb52d6a386320a8121123`  
		Last Modified: Mon, 24 Jun 2024 22:18:58 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488718242432206ada8bbd6c04cbaa45a328831c446ede003c7bfb2715c9a963`  
		Last Modified: Mon, 24 Jun 2024 23:11:17 GMT  
		Size: 862.4 KB (862414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4404fccdfb2b1fded0e6f55b4c62988302c45beb9372dc2002816352eaf0baa2`  
		Last Modified: Mon, 24 Jun 2024 23:11:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7891530bec860860360e01a55af6b8ddf1615f939d51e054b2850c8a9d65c91e`  
		Last Modified: Mon, 24 Jun 2024 23:11:18 GMT  
		Size: 13.6 MB (13640315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c034ef6fe1634e4e635a4cc5eacd8ebd48e2078fc13ae581fdd1c01c1ddfcb`  
		Last Modified: Mon, 24 Jun 2024 23:11:17 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-20-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:c3400865e5dc20437d66c882759ecced7bb3ee3a5992537f1f68fd506cf2bb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.8 KB (867802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8539ced7ff5ce2e13a7ef225efe28d051697ff935168f831567f1bc05589a28`

```dockerfile
```

-	Layers:
	-	`sha256:8cdf0e7f8e062d7a82dd28253e349e4c42b0da7bb014b0e1665a817d54873b2f`  
		Last Modified: Mon, 24 Jun 2024 23:11:17 GMT  
		Size: 852.1 KB (852135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95ddbe53429cb9c0eabf93f50097680efe394c44970c84e51bc173a8b0f7b019`  
		Last Modified: Mon, 24 Jun 2024 23:11:17 GMT  
		Size: 15.7 KB (15667 bytes)  
		MIME: application/vnd.in-toto+json

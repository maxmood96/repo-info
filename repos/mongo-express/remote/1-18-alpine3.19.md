## `mongo-express:1-18-alpine3.19`

```console
$ docker pull mongo-express@sha256:7b4471277e3b8b91c53931bd96bed1a1a550759dfc1c864b874217fbdc7a3acd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo-express:1-18-alpine3.19` - linux; amd64

```console
$ docker pull mongo-express@sha256:96f81d04fe1a87487bdfee681eac5dddebe7478e9edc0f255da62d90a17a7f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59326476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30928e2b25b286bd229e64ee3a803d6e8372cd4d92b32d7c59adc7fd8c0303eb`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.5
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="deaf95aceeb446d8861419884fc1d07c54e4a958e4d9b82d8fb9c8f1f7001535" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
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
	-	`sha256:6a5ba5322b4a5416240b08583db88aae9b9138dd36fd54aa9d20173c3db57851`  
		Size: 40.1 MB (40091144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c4a69072cc1e5ba000ae076927371dc1d755805dfc729ae27814d9b8ada2f`  
		Last Modified: Mon, 18 Nov 2024 15:04:47 GMT  
		Size: 1.4 MB (1387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36d32de04200f805172fdaa1bbe7a28053ec150a9b4cc181803fa3f44d8be09`  
		Last Modified: Mon, 18 Nov 2024 15:04:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c95f43c9c0d185eac3af16bbbce22a0dd6da90755336ed47bc5e1bcbb4d68a`  
		Last Modified: Mon, 18 Nov 2024 15:48:26 GMT  
		Size: 784.6 KB (784634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d602a51d2d6283f86cf1c7b7422215e556fb63806c44ad39190e3e886dfe5a2`  
		Last Modified: Mon, 18 Nov 2024 15:48:26 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff42aa84a81566c31473dc475f128e98f729357cdf0a8d7b9a5efc6ab9e6a14`  
		Last Modified: Mon, 18 Nov 2024 15:48:27 GMT  
		Size: 13.6 MB (13642358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5cdb5abafdf79efe06b7c427a363b9e80e585cf1456fc20681ceba4d9e3a96`  
		Last Modified: Mon, 18 Nov 2024 15:48:26 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-18-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:f344c8c7d4491248908e8ab6bc49b23501169aa90c260c6aeae781a0a7fa3f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000f356f8403e14d3d35901fd72a15305c9bfe502a1d6954d003cc2338a2bf0b`

```dockerfile
```

-	Layers:
	-	`sha256:5c68ff27ea04646ca72d4380c7b2b6cc5dcda1b0cd66ded85d6f17056e850b7e`  
		Last Modified: Mon, 18 Nov 2024 15:48:26 GMT  
		Size: 997.0 KB (996978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0637371154a2e15aa86e382289653d361827fb1eccec4ceec2b20a8be186903`  
		Last Modified: Mon, 18 Nov 2024 15:48:26 GMT  
		Size: 15.3 KB (15298 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo-express:1-18-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull mongo-express@sha256:c8c577f7294cb472ed605828362a28ff5f18683998acfc48e0caa156ac943019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58867067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cc64ee2a44d3bf2f2994320ae926f471235d5365da14287a710597e4a0168b`
-	Entrypoint: `["\/sbin\/tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["mongo-express"]`

```dockerfile
# Fri, 08 Mar 2024 19:22:05 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 08 Mar 2024 19:22:05 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2024 19:22:05 GMT
ENV NODE_VERSION=18.20.5
# Fri, 08 Mar 2024 19:22:05 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="deaf95aceeb446d8861419884fc1d07c54e4a958e4d9b82d8fb9c8f1f7001535" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
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
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145d210cb54045f3c727468bf465a3f263ff707a64da19e7d5d7f39680534637`  
		Last Modified: Mon, 18 Nov 2024 17:21:20 GMT  
		Size: 39.6 MB (39614415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbc6f17d6ed2208b0d690e9e6ca3e3704177f4bbf02182a206951021f7b401c`  
		Last Modified: Mon, 18 Nov 2024 17:21:19 GMT  
		Size: 1.4 MB (1387220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628a8cd3385e1d2063448f845b9b3f70a2834e0ceb45f5e0a035e2a39d5e51bc`  
		Last Modified: Mon, 18 Nov 2024 17:21:18 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45238959f1ddf4f8497f26c496c6ba336b080e2a6f03844c19e91abf1ded8da`  
		Last Modified: Mon, 18 Nov 2024 17:54:44 GMT  
		Size: 862.4 KB (862429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab29e44416606b4a2c9871028c57b693bc8ba40878d3463ce1edc04055711494`  
		Last Modified: Mon, 18 Nov 2024 17:54:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550b5e0a2b64253f23ab92f4205fb59bbf861a587832877f1597a542e4d543e8`  
		Last Modified: Mon, 18 Nov 2024 17:54:44 GMT  
		Size: 13.6 MB (13642367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d751af38797f0880970be4ba5a4924a6811d8df49c50fbe7ca5b8c97834c5240`  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo-express:1-18-alpine3.19` - unknown; unknown

```console
$ docker pull mongo-express@sha256:f9070ffc8df8e257a9cd62c4a485ce66ca8d45577706aabbd3d111ca86b19ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7f2f4220e0a08fe8f447522dc2e4d5aa0c7d90717a53bd981528a1d7da7c8d`

```dockerfile
```

-	Layers:
	-	`sha256:f21965d123e5277b344e97d00c458f44c0d749408d8e156096ce5ba7c8bcb229`  
		Last Modified: Mon, 18 Nov 2024 17:54:44 GMT  
		Size: 997.0 KB (997022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98b791c6fe3a2684f0753e7811a851a1fc18eaa6b3a81580f1b165b64af68ae0`  
		Last Modified: Mon, 18 Nov 2024 17:54:43 GMT  
		Size: 15.4 KB (15405 bytes)  
		MIME: application/vnd.in-toto+json

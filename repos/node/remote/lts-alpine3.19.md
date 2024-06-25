## `node:lts-alpine3.19`

```console
$ docker pull node@sha256:f28ec01ebb46af85d5a5c02f59296ccc494386da07d0a447a1b9f58fc8642167
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `node:lts-alpine3.19` - linux; amd64

```console
$ docker pull node@sha256:ef843b7b23094ac5d02bab48edc7d9965553b17285df320599b91b4646643f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46997871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c46a68a50da15c67c6187785fb6c60d41c0cd4361262d1310e59ee549d5a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
ENV NODE_VERSION=20.15.0
# Mon, 24 Jun 2024 14:33:35 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="24a21bc2fd2caf300ea36d716fbfa29ababa8a41bb844e67b6cf8b3d5091792c" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV YARN_VERSION=1.22.22
# Mon, 24 Jun 2024 14:33:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1d2f9462df5ec6396b71ecc7a9c988b7e16553553b15420e11051424d6a71c`  
		Last Modified: Mon, 24 Jun 2024 21:54:28 GMT  
		Size: 42.2 MB (42192865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a88c8b49c72f15046a57c2afd2c3a281f5ccde4fbdbbaf94328413e35523d88`  
		Last Modified: Mon, 24 Jun 2024 21:54:27 GMT  
		Size: 1.4 MB (1387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7257f487e1ba064f77fcc29f69c3bdaad16ae2ce39e9963b02cfbe05f5eb73`  
		Last Modified: Mon, 24 Jun 2024 21:54:26 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:2a889cefe928683fd0e4d67559852a9e5d3a2d12ffe41918f797cfc14a08313d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 KB (348760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:315d7b24adf3442c287f466c6769ad2b5b3a78f827a2c0f8d9ec29d0d5a7ebdd`

```dockerfile
```

-	Layers:
	-	`sha256:8a4f9ab40aecdec34daf04b74180c6d5af8d5bd5db82948876fe2faa8b3c7b97`  
		Last Modified: Mon, 24 Jun 2024 21:54:27 GMT  
		Size: 324.6 KB (324565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a497eb1aa8f795d6e3d0fa011c0cbc027d5eacf8a267ea8695a7d4f430e6709`  
		Last Modified: Mon, 24 Jun 2024 21:54:26 GMT  
		Size: 24.2 KB (24195 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-alpine3.19` - linux; arm variant v6

```console
$ docker pull node@sha256:8da566c468ceb13b88d287158c55f4dc27362db9c73333496b4940539cd6f5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45338703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d973daced5a0d2744bac0e9c02bbf0a2b60c83c7d7d576346d81141e824561e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
ENV NODE_VERSION=20.15.0
# Mon, 24 Jun 2024 14:33:35 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="24a21bc2fd2caf300ea36d716fbfa29ababa8a41bb844e67b6cf8b3d5091792c" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV YARN_VERSION=1.22.22
# Mon, 24 Jun 2024 14:33:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345709ffbb67025a9e4d92de7f44a0d57ef42e462f12ce6101a20af25ea4ffc1`  
		Last Modified: Mon, 24 Jun 2024 22:44:21 GMT  
		Size: 40.8 MB (40777126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98b0afc6005b60b820f15458e661dffe017204d275c80fb5638b37278c9d5ee`  
		Last Modified: Mon, 24 Jun 2024 22:44:23 GMT  
		Size: 1.4 MB (1387219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0b8d93727096e0af449af697afe4de9eb7814fcf7b476db21b5d3a881fde89`  
		Last Modified: Mon, 24 Jun 2024 22:44:20 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:8ad2680e2816cec0d819ed24ef1cceafe7f99286615421047e1b53baabc3f52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 KB (24066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0905a6d367a76db41e53398a90d1432c2758714f8e0abf5b1565b5ad7ede96`

```dockerfile
```

-	Layers:
	-	`sha256:00eefa341b341eea44ae021f14b08e46e1461e2f4bfd3d318154a4314794bb4d`  
		Last Modified: Mon, 24 Jun 2024 22:44:22 GMT  
		Size: 24.1 KB (24066 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-alpine3.19` - linux; arm variant v7

```console
$ docker pull node@sha256:2d32ba4d2c6f8811d52c39cdd32997156f64147f60e71950899cff595d975ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44521760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5dd809d5e1849d55c6e506689501eccc8dbd922071fe471cdc17acb8dd1d61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 04 Jun 2024 13:58:27 GMT
ADD file:a79253a22e927307fa2edd1752e7945fd88afbb97c73bbbe771cc99947c0517a in / 
# Tue, 04 Jun 2024 13:58:27 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 13:58:27 GMT
ENV NODE_VERSION=20.14.0
# Tue, 04 Jun 2024 13:58:27 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="f0afca5a7f4857d06d960490b2af36f72b5dd08732776454e33514796d07bff1" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 04 Jun 2024 13:58:27 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Jun 2024 13:58:27 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Jun 2024 13:58:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 13:58:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 13:58:27 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:4007367bb0cf596fd27d2207989b3864272eb2e5caf7429c07e68abc3bd47b0c`  
		Last Modified: Thu, 20 Jun 2024 18:01:06 GMT  
		Size: 2.9 MB (2926498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c801681adce7338fea2b4f22e3c1941a0f23b63e0dfa921112ae00cbb3237a16`  
		Last Modified: Fri, 21 Jun 2024 09:08:23 GMT  
		Size: 40.2 MB (40207600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b70d80b212672c0bb1a8d9adbe3ad9c538f7860d709241567ba1203751172e8`  
		Last Modified: Fri, 21 Jun 2024 09:08:22 GMT  
		Size: 1.4 MB (1387213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b525044cb79ec64689d92b5b360d5befbefe0ffaa7b47a9abf0cbc60f287a1`  
		Last Modified: Fri, 21 Jun 2024 09:08:22 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:6205ab256328723ddd4299661d108150f0c948bd06ba3322b9635bcea2e84ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 KB (348895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401720327dbcc5ed6ebb8a7c35742db0e48beb2dc25c92ca7201c868bbc5d220`

```dockerfile
```

-	Layers:
	-	`sha256:40c2c05d6e5713e3e566b720aceeb7d97fc6cac30d33897dc82ae846f9606e51`  
		Last Modified: Fri, 21 Jun 2024 09:08:22 GMT  
		Size: 324.6 KB (324609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d01340c60fb43d5a86d62958a472d7e0ceab399d8af4aeb6586cac41f115a3bc`  
		Last Modified: Fri, 21 Jun 2024 09:08:22 GMT  
		Size: 24.3 KB (24286 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull node@sha256:944206baf9e76b0cfac2a77b0cd713aa2dc688879f32a8d77a2c184d7157d302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46749472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b72a95d0d68aebe9417b0ec8e560504112578e884d78a8180e6280526edefcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
ENV NODE_VERSION=20.15.0
# Mon, 24 Jun 2024 14:33:35 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="24a21bc2fd2caf300ea36d716fbfa29ababa8a41bb844e67b6cf8b3d5091792c" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV YARN_VERSION=1.22.22
# Mon, 24 Jun 2024 14:33:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
CMD ["node"]
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

### `node:lts-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:e6289f89a4d4618355d698eb4fbe86f86789352761c935fbce16f0e1f35f0da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.1 KB (349140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6022c8145b36cf520af89669c9ca8a8ccd5917c129b6d35e606119e3f99dc6d`

```dockerfile
```

-	Layers:
	-	`sha256:b2b823208fbb3e086462f40be052131586fd0bd4524b76a00f48f0cad06b55b9`  
		Last Modified: Mon, 24 Jun 2024 22:18:58 GMT  
		Size: 324.6 KB (324633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf24e0cf62c4bb0696667471ad0d29081569e7a40304007c1d1d30391200766`  
		Last Modified: Mon, 24 Jun 2024 22:18:58 GMT  
		Size: 24.5 KB (24507 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-alpine3.19` - linux; ppc64le

```console
$ docker pull node@sha256:733e3d47ff467a160422ff68d93c33bdc15334d641834b6a8cfc3a6675606b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49828044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93349a485abe198ab1a827065a88dc090800f0092b47f976cffaeab951aefd8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
ENV NODE_VERSION=20.15.0
# Mon, 24 Jun 2024 14:33:35 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="24a21bc2fd2caf300ea36d716fbfa29ababa8a41bb844e67b6cf8b3d5091792c" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV YARN_VERSION=1.22.22
# Mon, 24 Jun 2024 14:33:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3731c4de9df81c2fe1c68c1d829aaf41a40827e424cdbe572e51b338cbc88046`  
		Last Modified: Mon, 24 Jun 2024 22:09:36 GMT  
		Size: 45.1 MB (45079745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09af94e6ee48231c841a33d749f23599d4547bb592d65e1c7440d30b0b669877`  
		Last Modified: Mon, 24 Jun 2024 22:09:35 GMT  
		Size: 1.4 MB (1387215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebabf735d2e4b9ab5a08ae071f655914d15dcfa150ea14a8545ca474cd6051fa`  
		Last Modified: Mon, 24 Jun 2024 22:09:34 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:c723718882485e0463b4e8436fe09e3021ba3ff12c93ae4554de5ebcffec9701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.9 KB (346892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1969d0e185748669b1a0bb98363125d9198680c92d65117fbb19dcb8e6438cad`

```dockerfile
```

-	Layers:
	-	`sha256:3021f4ab753040fec362bddfd8c510adf9ef46f003b5b08c531626a60fd7f8b7`  
		Last Modified: Mon, 24 Jun 2024 22:09:34 GMT  
		Size: 322.7 KB (322651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ffc8a522d1624344b4fdfb602eca405ff6f715c076dc9bdb186482ec4e1d034`  
		Last Modified: Mon, 24 Jun 2024 22:09:34 GMT  
		Size: 24.2 KB (24241 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-alpine3.19` - linux; s390x

```console
$ docker pull node@sha256:332aa9c76bafb173fe77d0c9f5dde629eaf685a6f3005a3800563b6fa45eeaee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48087419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a75732d75c08735909452ebdd2fd24624f938af448e2849f51f953afdef5b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
ENV NODE_VERSION=20.15.0
# Mon, 24 Jun 2024 14:33:35 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="24a21bc2fd2caf300ea36d716fbfa29ababa8a41bb844e67b6cf8b3d5091792c" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       61FC681DFB92A079F1685E77973F295594EC4689       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0       CC68F5A3106FF448322E48ED27F5E38D5B0A215F     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV YARN_VERSION=1.22.22
# Mon, 24 Jun 2024 14:33:35 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0017c7ebfe906fce4f50a13be5cbb474493f258812c6bbb555b6f5eb730b3`  
		Last Modified: Mon, 24 Jun 2024 22:32:43 GMT  
		Size: 43.4 MB (43447277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5250b14dcd4207c1515a7f98d1dd392ccd9687566ade1548d864a62334839c24`  
		Last Modified: Mon, 24 Jun 2024 22:32:43 GMT  
		Size: 1.4 MB (1387203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1589ddf5ec6a7e963703e281b1568ec2d81e0ae22f00932cbc40b1b6e01e271a`  
		Last Modified: Mon, 24 Jun 2024 22:32:42 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:7c1e3cf4a4d0c37b92ddebeee8ea92cf93d9b238eb172293ca4ddde3c32b3d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.8 KB (346806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992a87582b9ed3642053d4f95d7fb31946759495f51759e7f7869294c2dcdd20`

```dockerfile
```

-	Layers:
	-	`sha256:07452984234946b681842ea827e6c5d7adb3fa58775d15f87d312d2a3e64a18e`  
		Last Modified: Mon, 24 Jun 2024 22:32:42 GMT  
		Size: 322.6 KB (322611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7a9f31d2eee72754edfd66e651c000a1e7520ed6221ae4d871c28da9cc1c48e`  
		Last Modified: Mon, 24 Jun 2024 22:32:42 GMT  
		Size: 24.2 KB (24195 bytes)  
		MIME: application/vnd.in-toto+json

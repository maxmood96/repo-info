## `node:alpine3.20`

```console
$ docker pull node@sha256:c552bc1e86fc46128dfe003c86d4cbd0ada6254ac356c662b441ad95da8c4b2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `node:alpine3.20` - linux; amd64

```console
$ docker pull node@sha256:62b83d81bb0ea12664e7b0f89a905b102f20b3ce95c0bb64cf50fa4b69c42dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57846305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c49ef03a4c17feb83c51db19087e0d1059e517aa03bdcee6d7bc35a83cbb81b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 20:15:24 GMT
ENV NODE_VERSION=24.0.0
# Tue, 06 May 2025 20:15:24 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5c96f5245c8788665cc67f4962d6e94a8f50fb771563b206e135c14c9d8e5768" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Tue, 06 May 2025 20:15:24 GMT
ENV YARN_VERSION=1.22.22
# Tue, 06 May 2025 20:15:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 06 May 2025 20:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 May 2025 20:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 May 2025 20:15:24 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b171951831969c37012345df13e22b3df57aa624dc4eb360b3f13f064ad9b8`  
		Last Modified: Tue, 06 May 2025 20:53:52 GMT  
		Size: 52.8 MB (52831526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf232327398dc7a7400c320426e2ba06f7be43fc12ca6e1502d832d4bfe87dc`  
		Last Modified: Tue, 06 May 2025 20:53:51 GMT  
		Size: 1.4 MB (1387436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073d5f9bd71b6fda454dfcebcc88014ccbf377df14994ed3ee974c315472bc4d`  
		Last Modified: Tue, 06 May 2025 20:53:51 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:alpine3.20` - unknown; unknown

```console
$ docker pull node@sha256:4d46cdbcaaa2fb786c63dc34e8fb99c5c9952514c5f51b7c2e1251af10e3fc1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 KB (398489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a35114bedde7c77e065c3f63f39d93747dcdf513140a0e1e6c2e3cf3a6a0e83`

```dockerfile
```

-	Layers:
	-	`sha256:bc8a1d021cb2ef46ef5b84e6a3fc8cc7b72b3b012489fa84801ad97d2decca06`  
		Last Modified: Tue, 06 May 2025 20:53:51 GMT  
		Size: 374.6 KB (374588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80d51e7f7cd4b0cee0fa043135ee83942881649e9ddb5f45d7d4efef14f1ee7c`  
		Last Modified: Tue, 06 May 2025 20:53:51 GMT  
		Size: 23.9 KB (23901 bytes)  
		MIME: application/vnd.in-toto+json

### `node:alpine3.20` - linux; arm variant v6

```console
$ docker pull node@sha256:eac0587e618168862b74c8aa2fa58ee6008e46b4190c57e42f79f923e57a1fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54507638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5607052b7600373acad181f41c5d56b4ebc2afe1624bfadb37fb8fef64f7aab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:05:11 GMT
ENV NODE_VERSION=23.11.0
# Tue, 01 Apr 2025 16:05:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="d267e68a33036c2f3803adaf79b7191bcf45219cc12246f61c48b891bb70e943" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV YARN_VERSION=1.22.22
# Tue, 01 Apr 2025 16:05:11 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 16:05:11 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7833571550990da0a529fdc0f7c163d86ceedc8dadf8e54f553651dfbfe265d`  
		Last Modified: Tue, 01 Apr 2025 18:47:13 GMT  
		Size: 49.7 MB (49747166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1188a1c1acb23d40e0d9bad2c5d7723f085e951ede2d56b8583fa4b076f4ef95`  
		Last Modified: Tue, 01 Apr 2025 18:47:11 GMT  
		Size: 1.4 MB (1387494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffe0e7a0e46df0da65b0172d0171251b5a0da8a987a7265ad1d0e839ad55202`  
		Last Modified: Tue, 01 Apr 2025 18:47:11 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:alpine3.20` - unknown; unknown

```console
$ docker pull node@sha256:fd8f4a4fcca27892c1dace707d875afa3f29d52e9451e4b241d6bb8dd6928eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451fb7bc1df503dfe4c4cb0af5830b258f603d1b6ba4e5177a37c548c2d40cb7`

```dockerfile
```

-	Layers:
	-	`sha256:b9595c4f4286c2a37c2c076d0cdd0347e1ee421395136fb50922f4b616db4b3a`  
		Last Modified: Tue, 01 Apr 2025 18:47:11 GMT  
		Size: 23.7 KB (23692 bytes)  
		MIME: application/vnd.in-toto+json

### `node:alpine3.20` - linux; arm variant v7

```console
$ docker pull node@sha256:863ae6d1bf6f3906717d5703e22353006d2263749de1e9156914b9300b40409d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53577128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7342d79eef272a5f0a52c2e0f73da264c4e02a1b92e6fbbc73bc416c0b0ce417`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:05:11 GMT
ENV NODE_VERSION=23.11.0
# Tue, 01 Apr 2025 16:05:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="d267e68a33036c2f3803adaf79b7191bcf45219cc12246f61c48b891bb70e943" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV YARN_VERSION=1.22.22
# Tue, 01 Apr 2025 16:05:11 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 16:05:11 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69b91c644a14ea9bab5407a918329d29e45296cec9a00ed0c581b027a7cec7a`  
		Last Modified: Tue, 01 Apr 2025 19:16:00 GMT  
		Size: 49.1 MB (49093217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8ac4d281dab8bef027e134a4529db3ab88219edbaf6208c31111ebf9d912fa`  
		Last Modified: Tue, 01 Apr 2025 19:15:58 GMT  
		Size: 1.4 MB (1387497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194516ff96da03e29a04a60b9a50feee6efd39a52b493fe6f4875fc733ba2215`  
		Last Modified: Tue, 01 Apr 2025 19:15:58 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:alpine3.20` - unknown; unknown

```console
$ docker pull node@sha256:1f9fd71296f48b388f296030dc56d7a5d3ba7d575e40d049008f0f494b9a882d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.1 KB (407077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1c8c8f8fc68ef92d01a576b3fa0548f84cd1c6116c6eab7f765ee65569235a`

```dockerfile
```

-	Layers:
	-	`sha256:5c0ac1ead2da51e081253d8d2a50df288adc3675d443acaf12c6cb971f41337b`  
		Last Modified: Tue, 01 Apr 2025 19:15:58 GMT  
		Size: 383.2 KB (383170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d68311252e194a1ea5dc0f314725da0b381e50de6e0c9145c95a8a146afcb973`  
		Last Modified: Tue, 01 Apr 2025 19:15:58 GMT  
		Size: 23.9 KB (23907 bytes)  
		MIME: application/vnd.in-toto+json

### `node:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull node@sha256:b28da0b58d064df7b174ac7563171b4ee0ba1bcb8595986cb564b1b5efc907d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57482764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47d8905e4894e80c59b587ec2386282eb23465cbb57c7f7ce7e86bd266a0075`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 20:15:24 GMT
ENV NODE_VERSION=24.0.0
# Tue, 06 May 2025 20:15:24 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5c96f5245c8788665cc67f4962d6e94a8f50fb771563b206e135c14c9d8e5768" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Tue, 06 May 2025 20:15:24 GMT
ENV YARN_VERSION=1.22.22
# Tue, 06 May 2025 20:15:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 06 May 2025 20:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 May 2025 20:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 May 2025 20:15:24 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71928465395c5c64a19b1a25c8cf3ccdda34aef6f1a65a145ea73aa073345699`  
		Last Modified: Tue, 06 May 2025 21:49:26 GMT  
		Size: 52.0 MB (52003716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd14fe1b105aa6e5d3c56f565cd46ad6bbe24d051f322bc725e49eb940d896d6`  
		Last Modified: Tue, 06 May 2025 21:49:25 GMT  
		Size: 1.4 MB (1387438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5251f7983817ce0291fbfdcbd5a215aa8033fbbbaf2ab8b1c8d13021eb454743`  
		Last Modified: Tue, 06 May 2025 21:49:24 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:alpine3.20` - unknown; unknown

```console
$ docker pull node@sha256:2bc0b8a7bf190a84d8dcfe71ecae7ad423f4823d43419d2fb504b6a310d641b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 KB (398690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1f2c4225448280d3b10a2c0ed5021854e6b4d0b3a01ceae1a33c595fad8644`

```dockerfile
```

-	Layers:
	-	`sha256:40d053ab53851818de8eb949579f174fac8af572777bffa361615255b9f000c3`  
		Last Modified: Tue, 06 May 2025 21:49:24 GMT  
		Size: 374.7 KB (374656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb7944685074571c4c25b199e7011cd0a6e8441d71b8bc1f13707d2818a3a3a1`  
		Last Modified: Tue, 06 May 2025 21:49:24 GMT  
		Size: 24.0 KB (24034 bytes)  
		MIME: application/vnd.in-toto+json

### `node:alpine3.20` - linux; s390x

```console
$ docker pull node@sha256:f9f8ddbc8d477b8a0e2bb896e31400f2d3215adb89b11ea3d384f4eb2d0858db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57945318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faad2926598506636cee89bd249d531a7c1c34223362850c2cfe43b051f740f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:05:11 GMT
ENV NODE_VERSION=23.11.0
# Tue, 01 Apr 2025 16:05:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="d267e68a33036c2f3803adaf79b7191bcf45219cc12246f61c48b891bb70e943" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV YARN_VERSION=1.22.22
# Tue, 01 Apr 2025 16:05:11 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 16:05:11 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9665e61949e137c0a3556fb594857b92fa691d570af8434a06d10e1e0fd2cd92`  
		Last Modified: Tue, 01 Apr 2025 23:54:12 GMT  
		Size: 53.1 MB (53093254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082f77be0082beb83ae7d7d807327208bcb8b402c35d0fb28a97e5d72406e6bb`  
		Last Modified: Tue, 01 Apr 2025 23:54:11 GMT  
		Size: 1.4 MB (1387495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f24dee6430ebf8d934d04e460e6e30d96a992db1ed0afde7779681404a600`  
		Last Modified: Tue, 01 Apr 2025 23:54:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:alpine3.20` - unknown; unknown

```console
$ docker pull node@sha256:3c355d55999aee2124764bb5930feb18013a36d092f215461a129a7c39258fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.0 KB (404985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94bb7bdb56282986c154081edc7b6fb7f254a037468d01d5336f53509c4a5d3`

```dockerfile
```

-	Layers:
	-	`sha256:b277bf48cbb32625a0a8df64dc5e94fb076a6381f360e8366a48177385ba904b`  
		Last Modified: Tue, 01 Apr 2025 23:54:11 GMT  
		Size: 381.2 KB (381175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77a850465db3424d408c765d1f524da88e54b352bc30b9a17013e432d51cba1e`  
		Last Modified: Tue, 01 Apr 2025 23:54:11 GMT  
		Size: 23.8 KB (23810 bytes)  
		MIME: application/vnd.in-toto+json

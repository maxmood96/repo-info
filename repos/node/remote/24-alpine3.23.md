## `node:24-alpine3.23`

```console
$ docker pull node@sha256:682368d8253e0c3364b803956085c456a612d738bd635926d73fa24db3ce53d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `node:24-alpine3.23` - linux; amd64

```console
$ docker pull node@sha256:b3c2a6ebd4b9b3d1a3f8a58252c07b680e442e61ce1306ebdbc408ddf27cec14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56063689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa855d560496a2dc8ca38f060c113e0651cdde1cb6c794599a0e977f55d35382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 21:13:14 GMT
ENV NODE_VERSION=24.11.1
# Thu, 04 Dec 2025 21:13:14 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="825c670d7212b6d5a04f8b2462bb3fd4f15cc5842a7e934de307070e4408d2aa" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 04 Dec 2025 21:13:14 GMT
ENV YARN_VERSION=1.22.22
# Thu, 04 Dec 2025 21:13:17 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 04 Dec 2025 21:13:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 21:13:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 21:13:17 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea370b117ea66438d0bc154a347a2f5de4816e445e2b061001161310b4f00d58`  
		Last Modified: Thu, 04 Dec 2025 21:13:44 GMT  
		Size: 50.9 MB (50941827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de13c80ec1f1c2868b7daab769f3d7cb1bfb2bb16142918a157fd6324bc1ee59`  
		Last Modified: Thu, 04 Dec 2025 21:13:38 GMT  
		Size: 1.3 MB (1262102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f196bed839b234bc062fab82e6ee8c6f7cdc22a6ceb81180a4ceb4b08bb6cb`  
		Last Modified: Thu, 04 Dec 2025 21:13:41 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:24-alpine3.23` - unknown; unknown

```console
$ docker pull node@sha256:620da755b2e2c4f6971d8e99626d1a67c49075d868ce896fdc58d802cfe03050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.0 KB (400021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b6f1002388a88f20884da1e2eb12ba25048e0649d4a151dda0e237d5b8dffa`

```dockerfile
```

-	Layers:
	-	`sha256:d54be48aa3f6b1bc35548924c3d029d7d9d71cb7acb53e1f2b0b5739308f4d09`  
		Last Modified: Thu, 04 Dec 2025 22:41:57 GMT  
		Size: 374.2 KB (374187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6285b4062078f40daa06e076721b2de5f962c71339edbd4778d1f2790f94416`  
		Last Modified: Thu, 04 Dec 2025 22:41:57 GMT  
		Size: 25.8 KB (25834 bytes)  
		MIME: application/vnd.in-toto+json

### `node:24-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull node@sha256:f4a1ba23ca013418f51f7d4d4673d8f8797241b68c05436a8825031a84c9f4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57299560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac71958c4504538303efbc81234996c7c60e4c3b64d78a538c4cc7bf52c068c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 21:49:09 GMT
ENV NODE_VERSION=24.11.1
# Thu, 04 Dec 2025 21:49:09 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="825c670d7212b6d5a04f8b2462bb3fd4f15cc5842a7e934de307070e4408d2aa" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 04 Dec 2025 21:49:09 GMT
ENV YARN_VERSION=1.22.22
# Thu, 04 Dec 2025 21:49:12 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 04 Dec 2025 21:49:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 21:49:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 21:49:12 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c845fdaca6c4d744a5e627b67e202e621ad0d70c05098b5e4b3578d9ae18b3`  
		Last Modified: Thu, 04 Dec 2025 21:49:45 GMT  
		Size: 51.8 MB (51840924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dcc37482cbf0f6005b5410ace90505fd516157bda69fc3ca0f8bc8b62155b5`  
		Last Modified: Thu, 04 Dec 2025 21:49:34 GMT  
		Size: 1.3 MB (1262991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a880a9613a5ad1fe022e38d945957d51a365d788257f320025d93342a1948347`  
		Last Modified: Thu, 04 Dec 2025 21:49:34 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:24-alpine3.23` - unknown; unknown

```console
$ docker pull node@sha256:4a6cd9de7105c5a0ad1044578b146d4acb81d3603a112a7adb412b69dbeee1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.7 KB (399690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dc41e632708335bae2cd91c9111e497a8019cb25b7f514ad4d2f39e2debcf0`

```dockerfile
```

-	Layers:
	-	`sha256:5bb9850fc8a36b7b1615d98eac44703bfdaf99cfd8e2f9a05c884121c36e825b`  
		Last Modified: Thu, 04 Dec 2025 22:42:00 GMT  
		Size: 373.7 KB (373665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1160a3e9ea81a4ada6a5742ba2c0c3b729ff431b879c88fa25afb9c04f89b743`  
		Last Modified: Thu, 04 Dec 2025 22:42:01 GMT  
		Size: 26.0 KB (26025 bytes)  
		MIME: application/vnd.in-toto+json

### `node:24-alpine3.23` - linux; s390x

```console
$ docker pull node@sha256:c9b3b402d14e7012a1f4bd132aa99bb1eec2383a6df4a201fe4477e125cad854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57448566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8430e17502d48b160628aaf6c8ffbab3f0761a6acbdc2c805582bd0b6c1b6b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 23:22:45 GMT
ENV NODE_VERSION=24.11.1
# Thu, 04 Dec 2025 23:22:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="825c670d7212b6d5a04f8b2462bb3fd4f15cc5842a7e934de307070e4408d2aa" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 04 Dec 2025 23:22:45 GMT
ENV YARN_VERSION=1.22.22
# Thu, 04 Dec 2025 23:22:54 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 04 Dec 2025 23:22:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 23:22:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 23:22:55 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf5dffed4dd6c1b34469b059368c26ab50012f03fbe8ed57d319d63cb2b7922`  
		Last Modified: Thu, 04 Dec 2025 23:23:48 GMT  
		Size: 52.5 MB (52461339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d336d629adf5e8d0b68ac4f81673a088e4316cd186c8105d3483ad6b4b9bf2`  
		Last Modified: Thu, 04 Dec 2025 23:23:42 GMT  
		Size: 1.3 MB (1262970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8fcd20ed01ddfafe8bf60c009128e3bbe8e14f89a0e68af146182d4bc05fd4`  
		Last Modified: Thu, 04 Dec 2025 23:23:42 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:24-alpine3.23` - unknown; unknown

```console
$ docker pull node@sha256:65fae3deb82e74ca6a986467843c66708b82db0a39e0ddd952f880a971e969a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.4 KB (399370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639e29cc83ff360a387be360862d1c5ed5951d7bf1c7bfbb9be0decb14ce40e8`

```dockerfile
```

-	Layers:
	-	`sha256:1f8e2cef692962d6ca2d5c02979aa2bf813154f4eb84c89854a53368f713ad5f`  
		Last Modified: Fri, 05 Dec 2025 01:39:38 GMT  
		Size: 373.5 KB (373536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a70564e39a77372f786a8d75caa283730c20b0e3caee1187b10a867ba18c559`  
		Last Modified: Fri, 05 Dec 2025 01:39:39 GMT  
		Size: 25.8 KB (25834 bytes)  
		MIME: application/vnd.in-toto+json

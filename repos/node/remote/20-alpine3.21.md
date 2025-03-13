## `node:20-alpine3.21`

```console
$ docker pull node@sha256:0ede981d08de58d43bee3524a45e9446d20593af2c26fe97bb3ef930a2d08309
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

### `node:20-alpine3.21` - linux; amd64

```console
$ docker pull node@sha256:37a5a350292926f98d48de9af160b0a3f7fcb141566117ee452742739500a5bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47853495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5885a9462a2f940d7b54cb56ee6eee1943d7fbdcbf0cc1fdf074cf3eab807241`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 13 Mar 2025 14:48:02 GMT
ENV NODE_VERSION=20.19.0
# Thu, 13 Mar 2025 14:48:02 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2a58593a9de31ca444fe095cb2db0674bdccab426ee6803110ca17867bdac26" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
ENV YARN_VERSION=1.22.22
# Thu, 13 Mar 2025 14:48:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Mar 2025 14:48:02 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc209e5911cb71400e7dcbfccf23b57aebf6f4a308f6870a67d99d464426e2e`  
		Last Modified: Thu, 13 Mar 2025 17:08:33 GMT  
		Size: 43.0 MB (42950229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a069a788e09c70b6e7bd23a40de8714784738174cb975e7a9a20f3ae2be24b`  
		Last Modified: Thu, 13 Mar 2025 17:08:32 GMT  
		Size: 1.3 MB (1260570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ec265e2954eaadbe3a9ad5bb4b55b8713189b49ad9cc1c0c9eac64ec479363`  
		Last Modified: Thu, 13 Mar 2025 17:08:32 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-alpine3.21` - unknown; unknown

```console
$ docker pull node@sha256:a7ed39f60555cffaea0232bf793bc447570575511a4e2689160fdf755bdfdaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.2 KB (397216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a252902dd77a9ce12c3ea4e6e4d602e17d9f6e7daeccd4cc2b039f7fb009b2`

```dockerfile
```

-	Layers:
	-	`sha256:32f14cd8a33b3a37350d1c57e1cf7c5998c2a2b6ece0b600107cd4290029f16f`  
		Last Modified: Thu, 13 Mar 2025 17:08:32 GMT  
		Size: 372.5 KB (372494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:262c785881c8341161decac120d93925fe49c6c12e4691098c72ba2ef4f2d6bf`  
		Last Modified: Thu, 13 Mar 2025 17:08:32 GMT  
		Size: 24.7 KB (24722 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-alpine3.21` - linux; arm variant v6

```console
$ docker pull node@sha256:879a730e4097c266cb050bacdc91590e6afdc154eec9057a22920c85c0ef68f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45539516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1112cb373633855703bcf89f5b1aa77cd9badbbadae5573a13e5234158b3c85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 10 Feb 2025 15:34:31 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
ENV NODE_VERSION=20.18.3
# Mon, 10 Feb 2025 15:34:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="e559c7e9fbaca994cdf25f116257bd5e48851f82eeddbc1a56857a1f9a58d882" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENV YARN_VERSION=1.22.22
# Mon, 10 Feb 2025 15:34:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919af1fcfab4af8cc402fa84d7bfe2f94dcd68fa3cf513fa8a4b80bf190e6fb8`  
		Last Modified: Sat, 15 Feb 2025 06:25:40 GMT  
		Size: 40.9 MB (40913776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdfce423a9aba2ddefd70bae9c4b8ce97e7b2aca1cc4545a6d29d9560643c47`  
		Last Modified: Sat, 15 Feb 2025 06:25:39 GMT  
		Size: 1.3 MB (1260562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ace0483f02a32e223e94164c01cde5b7532d1d97ba27f7e27da36eb0ad3ba4`  
		Last Modified: Sat, 15 Feb 2025 06:25:39 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-alpine3.21` - unknown; unknown

```console
$ docker pull node@sha256:b16e9f23bcd1e10377e9f19e7d0c2fd3c20287f15af59ce0e4bb2ae3bec23b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 KB (24628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbd9b9ac6a06c3c4356b403309dafb39c10baa9bd7ea18a0d4922e0657df045`

```dockerfile
```

-	Layers:
	-	`sha256:7405ceff03e94d4d5a1a699844ff64eac725c4ab55573d0c1da196d780499487`  
		Last Modified: Sat, 15 Feb 2025 06:25:39 GMT  
		Size: 24.6 KB (24628 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-alpine3.21` - linux; arm variant v7

```console
$ docker pull node@sha256:5a3b1b3f051d4b99def82ab1026c924a1e935d180e84b559d8643278a661ff7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44729045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc32a3162c0582b90b9d878ee577da34cdac2af46c5539f0b2890302412eca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 10 Feb 2025 15:34:31 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
ENV NODE_VERSION=20.18.3
# Mon, 10 Feb 2025 15:34:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="e559c7e9fbaca994cdf25f116257bd5e48851f82eeddbc1a56857a1f9a58d882" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENV YARN_VERSION=1.22.22
# Mon, 10 Feb 2025 15:34:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7689a67d57913af9fa5059df2b8b82ceca1794c5b82322116443ca448a10e8`  
		Last Modified: Sat, 15 Feb 2025 06:14:58 GMT  
		Size: 40.4 MB (40369908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e30d76634c6fb21a92b2f2d479ab712b2e6ef12e096e70b3012574f9083efd`  
		Last Modified: Sat, 15 Feb 2025 06:14:57 GMT  
		Size: 1.3 MB (1260569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aa21d4f1a5a919283eb73250bdca67008022a290415d6ec7206a9550e0ddc1`  
		Last Modified: Sat, 15 Feb 2025 06:14:56 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-alpine3.21` - unknown; unknown

```console
$ docker pull node@sha256:c39dbaba15607f9ac8450c02021ea8a33a55a50f3cf111993fd3e1973a6d196a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 KB (397405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e36b2b161d5d5bc6793b32066c5bec7bae827c9db3b04d98111f876cd8ed9d`

```dockerfile
```

-	Layers:
	-	`sha256:e1f90890c24cbfb19aa61364ed7e957d1b04eff7af32f31f3e6c321298b2622e`  
		Last Modified: Sat, 15 Feb 2025 06:14:57 GMT  
		Size: 372.6 KB (372562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c4ebf0e2f0e4a8b36a2fae437f3ef7b766cc096f26c5122722e6e4b6797ea77`  
		Last Modified: Sat, 15 Feb 2025 06:14:57 GMT  
		Size: 24.8 KB (24843 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull node@sha256:646bc11400802534d70bc576fc9704bb6409e0ed802658a8e785472d160c38d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47881781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06038a15a690bf7aa19f84b6d7bf2646640654b47fd5d2dd8fca56ff81f0789`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 13 Mar 2025 14:48:02 GMT
ENV NODE_VERSION=20.19.0
# Thu, 13 Mar 2025 14:48:02 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2a58593a9de31ca444fe095cb2db0674bdccab426ee6803110ca17867bdac26" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
ENV YARN_VERSION=1.22.22
# Thu, 13 Mar 2025 14:48:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 14:48:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Mar 2025 14:48:02 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3e948a6346a46c6ad228463eb896bd63a271b9b122fc90d39a8702b2349746`  
		Last Modified: Thu, 13 Mar 2025 18:01:38 GMT  
		Size: 42.6 MB (42627714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfaf621f0ce4e4ddf5efac2af68a506ee03c6cb9151dd7f9b2b8937b3cfdfb5`  
		Last Modified: Thu, 13 Mar 2025 18:01:37 GMT  
		Size: 1.3 MB (1260594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d73ebbcecf2389cf3461a46c9a11972293f334e5093233adb4f1c65ef91e4e0`  
		Last Modified: Thu, 13 Mar 2025 18:01:37 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-alpine3.21` - unknown; unknown

```console
$ docker pull node@sha256:7b98f46e703c96cf1624e46f0b1d243f06a060aee9f10ee9fd49f2c4e592feee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.5 KB (397487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72360c44075aa98693e21b2cbefb86e640b38b0a519b76a877a13a9e3f973769`

```dockerfile
```

-	Layers:
	-	`sha256:ab8d3d7f6a045fe0dfdbde495343130be61774f88ce66a27353b529756870043`  
		Last Modified: Thu, 13 Mar 2025 18:01:37 GMT  
		Size: 372.6 KB (372598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54319906156895895ea72552d4e9c3ef3ffcbfe0ec38eabf3ebaaf0a2c2318a8`  
		Last Modified: Thu, 13 Mar 2025 18:01:37 GMT  
		Size: 24.9 KB (24889 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-alpine3.21` - linux; ppc64le

```console
$ docker pull node@sha256:8768e1171cb5be36d1fd22141b9734747acdb10f63f60b0a2e7e822897b43f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50188436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45833fedf8b6de769a6a76764b250a5f41a15a898e695a13297603c7a6f96cc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 10 Feb 2025 15:34:31 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
ENV NODE_VERSION=20.18.3
# Mon, 10 Feb 2025 15:34:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="e559c7e9fbaca994cdf25f116257bd5e48851f82eeddbc1a56857a1f9a58d882" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENV YARN_VERSION=1.22.22
# Mon, 10 Feb 2025 15:34:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3863c8b7444ee9e39bee466ac471c497a6f85cf69abd0196f6cbbf4847fa35`  
		Last Modified: Fri, 14 Feb 2025 22:43:32 GMT  
		Size: 45.4 MB (45353095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f5dbf12b5c87e4063dd7ed93fea10f46b65b269151d23d2562fb8159d763aa`  
		Last Modified: Fri, 14 Feb 2025 22:43:30 GMT  
		Size: 1.3 MB (1260552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913fe4b73c4c5ca62a6d627e004275f609372799e25353caa9908610a4a841cc`  
		Last Modified: Fri, 14 Feb 2025 22:43:30 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-alpine3.21` - unknown; unknown

```console
$ docker pull node@sha256:8493c9a6fa10f6637a9d5fed9f5d1d9395c7b4dc9822268df9ebdd1b94e590cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.4 KB (395393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79585eb5677473460e9423263f5cad2cae760e9ea9f177c901361862ae7c4027`

```dockerfile
```

-	Layers:
	-	`sha256:e0bd607ab1418346643f68092141dc0ead837a6b9397e175777cbea8dd730578`  
		Last Modified: Fri, 14 Feb 2025 22:43:30 GMT  
		Size: 370.6 KB (370601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51eb26a0fad47639fc55e9a94517596f491c2a3fa33e91de4f9b6d793fc9851d`  
		Last Modified: Fri, 14 Feb 2025 22:43:30 GMT  
		Size: 24.8 KB (24792 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-alpine3.21` - linux; s390x

```console
$ docker pull node@sha256:2e8849c14b984c6bb04de37cb6bfd765c3738cfff4e31333e825cfd8bc8430b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48512076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9caaaf356f58f4d9e070f0904253f8e5513c37fa3259b8b92bb23ca0c4e7c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 10 Feb 2025 15:34:31 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
ENV NODE_VERSION=20.18.3
# Mon, 10 Feb 2025 15:34:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="e559c7e9fbaca994cdf25f116257bd5e48851f82eeddbc1a56857a1f9a58d882" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENV YARN_VERSION=1.22.22
# Mon, 10 Feb 2025 15:34:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Feb 2025 15:34:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Feb 2025 15:34:31 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1e8e18b900f309c4d0353ec19692cbcbc75702efb763235c70b80de496ce89`  
		Last Modified: Sat, 15 Feb 2025 04:35:42 GMT  
		Size: 43.8 MB (43783521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d081763b808621757e031a19658d87e2f4182b5ee056d61b2e7be8764ae234dd`  
		Last Modified: Sat, 15 Feb 2025 04:35:42 GMT  
		Size: 1.3 MB (1260547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a63ae980372c5f622652f013020efbbb499f5a0d810a952689c01c60737061`  
		Last Modified: Sat, 15 Feb 2025 04:35:41 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-alpine3.21` - unknown; unknown

```console
$ docker pull node@sha256:fb25d8e687d3245f183344eccefb48b7481e71b15d46217dd0358d3c4ef49986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.3 KB (395265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56aee1ce7a053eea8510e2f5020438be4a57f93b7b8fe4bce3f83c46b3cce379`

```dockerfile
```

-	Layers:
	-	`sha256:b3a2985706a64e57cb1c57c738608c5bc7a136ea0113dd231241913183f76bc7`  
		Last Modified: Sat, 15 Feb 2025 04:35:41 GMT  
		Size: 370.5 KB (370543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01f236e3ebb9b67ac1fa805e295b6b0820d94e3cc4bb0b64810ff580ef054538`  
		Last Modified: Sat, 15 Feb 2025 04:35:41 GMT  
		Size: 24.7 KB (24722 bytes)  
		MIME: application/vnd.in-toto+json

## `node:current-alpine`

```console
$ docker pull node@sha256:ef080e3024ee76f0efee71f555cbf82e5a50bf8a89635fea3af200f59e7cb530
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

### `node:current-alpine` - linux; amd64

```console
$ docker pull node@sha256:9a8307ff9cc4ecce674ebb14afacf69d52f087daa8c9aa9d88f57d66036ee4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56414028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a13c8c01bd86d1c690853dc3b3e7a24153cf2ce27256d6807b1887d0b5eb5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 19 Dec 2024 20:48:00 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:48:00 GMT
ENV NODE_VERSION=23.5.0
# Thu, 19 Dec 2024 20:48:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a5631cbec5b8b3c3d45ad44d9195101799938d7ebde0d364b15de6a7f8d2e87a" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENV YARN_VERSION=1.22.22
# Thu, 19 Dec 2024 20:48:00 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Dec 2024 20:48:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Tue, 07 Jan 2025 19:42:27 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642c708256d026473576c155326a98773d5c34264561655e13d649ce8d8307be`  
		Last Modified: Tue, 07 Jan 2025 03:33:34 GMT  
		Size: 51.5 MB (51516716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75727f1325b06a0dd81ae29f657903a3a55ba2bf4b6a186143c546e635c33b03`  
		Last Modified: Tue, 07 Jan 2025 03:33:34 GMT  
		Size: 1.3 MB (1260644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa62612213c11903676e72b0bfade48f0d3c760bc03604bee35735bff45e122`  
		Last Modified: Tue, 07 Jan 2025 03:33:34 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-alpine` - unknown; unknown

```console
$ docker pull node@sha256:459932ce809a364a2d69db8e047a9e144062b40ca4140e54aaf1db7aae37a9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.6 KB (415604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bfd041db24dda7d2dae892ae5af5373037a3552fc89cf3cbe18d4f65f68f6a`

```dockerfile
```

-	Layers:
	-	`sha256:a20e9ef8b8ddcf1d5cae2976378d85f99c294f62cad50162aed3b2962be4968c`  
		Last Modified: Tue, 07 Jan 2025 03:33:34 GMT  
		Size: 390.3 KB (390284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac1523ce4230333ad1243b5d9773fdb169ad72bb65c78ecb9b9247e857067d9`  
		Last Modified: Tue, 07 Jan 2025 03:33:34 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-alpine` - linux; arm variant v6

```console
$ docker pull node@sha256:24c327281b8dcf736e5c61e127c408b053bfa0c14c13ca8db97cd1208f8be96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53931709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2548c7a9ad3cf56cb9d0f3053b725ffd8b4149a6030a412da4d73ae80ce96707`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 19 Dec 2024 20:48:00 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:48:00 GMT
ENV NODE_VERSION=23.5.0
# Thu, 19 Dec 2024 20:48:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a5631cbec5b8b3c3d45ad44d9195101799938d7ebde0d364b15de6a7f8d2e87a" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENV YARN_VERSION=1.22.22
# Thu, 19 Dec 2024 20:48:00 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Dec 2024 20:48:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a9dec548908931f6e534ff521313e672f61039ad0d99e6ebd33f26f8f57ad`  
		Last Modified: Tue, 07 Jan 2025 10:17:25 GMT  
		Size: 49.3 MB (49309615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6038c458854e47dbacb9e094c97f102cf859d4d22f2bb7d839f5ae56febe3450`  
		Last Modified: Tue, 07 Jan 2025 10:17:24 GMT  
		Size: 1.3 MB (1260613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbe61ca1c2fbbc77b6082fe69da86265ea91cae655a8720a60ec6ff0065d0b7`  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-alpine` - unknown; unknown

```console
$ docker pull node@sha256:17b795ec810e243afe6a6bc0ab61d41c8d889f34a6133ac66843478c571cbdaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f985e4653a0ebfede1552683b38db70df08a0ee20f1a535b062ba46d94110535`

```dockerfile
```

-	Layers:
	-	`sha256:1b0e7bd2b77fd78cbbc5556a7c755704521ecf5e12c7b614b6f7535ec284889c`  
		Last Modified: Tue, 07 Jan 2025 10:17:24 GMT  
		Size: 25.2 KB (25242 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-alpine` - linux; arm variant v7

```console
$ docker pull node@sha256:4fa6dab72fbe1770c0295423063fda78f9048c0571a50a7ba17fe0ce9824f85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53008150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c236004ca73989b61ebb597005c72e6230bfefa846f289fbed534b36e1ab08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 19 Dec 2024 20:48:00 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:48:00 GMT
ENV NODE_VERSION=23.5.0
# Thu, 19 Dec 2024 20:48:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a5631cbec5b8b3c3d45ad44d9195101799938d7ebde0d364b15de6a7f8d2e87a" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENV YARN_VERSION=1.22.22
# Thu, 19 Dec 2024 20:48:00 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Dec 2024 20:48:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31894062baa544a5d24f129b82b3303480c301c6a7ca41ca39ff933bb9f6725`  
		Last Modified: Tue, 07 Jan 2025 09:59:41 GMT  
		Size: 48.7 MB (48653848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ec3d50bfbda335588da1c77da8f4dcc98656bf8229ce90eb5c372285da0106`  
		Last Modified: Tue, 07 Jan 2025 09:59:40 GMT  
		Size: 1.3 MB (1260616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f3fe3e9640263cc8f91ddc82ee77bdb628a42ee64c3e20b6e2388cb4a6563`  
		Last Modified: Tue, 07 Jan 2025 09:59:40 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-alpine` - unknown; unknown

```console
$ docker pull node@sha256:ac1e73f52cc957f3009a67895c86e3e0c9ce06f5a1228baf80b7bc884c22fd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.8 KB (415825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7146d2be069139b43747444b7929a629e0978f0fe791d695b44b859c48c53d`

```dockerfile
```

-	Layers:
	-	`sha256:939365090bf85d016eef3277ea69242425bc6f289c3a0ba5d935f784f3321d07`  
		Last Modified: Tue, 07 Jan 2025 09:59:40 GMT  
		Size: 390.4 KB (390368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00dcc8504865599fde2410c7db841bbd7180a2f44bccd27a945ef863dc967c36`  
		Last Modified: Tue, 07 Jan 2025 09:59:40 GMT  
		Size: 25.5 KB (25457 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-alpine` - linux; arm64 variant v8

```console
$ docker pull node@sha256:de291c5e2d43d6249fc2d5c1035245b8705ee95f9a054a3bc5e93ea723e6926e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56068336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7ac00d46a372e97ca552619d1846c5c1e06b5b1efe2ca75a388f3abee0a880`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 19 Dec 2024 20:48:00 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:48:00 GMT
ENV NODE_VERSION=23.5.0
# Thu, 19 Dec 2024 20:48:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a5631cbec5b8b3c3d45ad44d9195101799938d7ebde0d364b15de6a7f8d2e87a" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENV YARN_VERSION=1.22.22
# Thu, 19 Dec 2024 20:48:00 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Dec 2024 20:48:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32afd7c5b6db1c0aca2428c1a397a1b6ae66d18ff1c235c676e9b83df9b7a3d7`  
		Last Modified: Tue, 07 Jan 2025 10:31:19 GMT  
		Size: 50.8 MB (50824229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fc0384adc7680ce456c7c92f1ec3d81db126943375db7c5c1d0e7c5f70ce2d`  
		Last Modified: Tue, 07 Jan 2025 10:31:18 GMT  
		Size: 1.3 MB (1260655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2580c9397268c8d90bf9a89b10f04af8aec827d1a3bcf95a8a7ea509a6f2a23f`  
		Last Modified: Tue, 07 Jan 2025 10:31:17 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-alpine` - unknown; unknown

```console
$ docker pull node@sha256:fee89cd3c3884a8cbc945c8270780c668718258d4b8168a8a462440ee25ce0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 KB (415923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0453d17ed98e2a2fd5c50ec2a779be370a3e7df023e12156b3fe4010a5272360`

```dockerfile
```

-	Layers:
	-	`sha256:cc61b04617e50b2f3cf11161b062272cb1c7885688a538e84d6358fefa726e5e`  
		Last Modified: Tue, 07 Jan 2025 10:31:17 GMT  
		Size: 390.4 KB (390412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5919fe156c93972489510cc69390db703f929fc6eadf1e1bf66448af79a1afb2`  
		Last Modified: Tue, 07 Jan 2025 10:31:17 GMT  
		Size: 25.5 KB (25511 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-alpine` - linux; s390x

```console
$ docker pull node@sha256:e37d2c64f1a67b71370a71083602a3d90943216c244a7857315333ce042c37cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57477154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c241707959c02f1b62cbec134304ad6868daf86772eb74c83f19980010346fe3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 19 Dec 2024 20:48:00 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
CMD ["/bin/sh"]
# Thu, 19 Dec 2024 20:48:00 GMT
ENV NODE_VERSION=23.5.0
# Thu, 19 Dec 2024 20:48:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a5631cbec5b8b3c3d45ad44d9195101799938d7ebde0d364b15de6a7f8d2e87a" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENV YARN_VERSION=1.22.22
# Thu, 19 Dec 2024 20:48:00 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Dec 2024 20:48:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ed5d4bea550e82fea38c2a50659a51a056b14af8e77bda9b712d9c6f74f4bd`  
		Last Modified: Tue, 07 Jan 2025 09:08:59 GMT  
		Size: 52.8 MB (52756640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48dbe091590a5e2d78f5b1f02d9566f908e6697758f702ebc3800e64eed89949`  
		Size: 1.3 MB (1260621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0992d59f35504c3a4f2f2bcaf51616d1a0c0cb1d6bfb5205bdb38387ec452a5`  
		Last Modified: Tue, 07 Jan 2025 09:08:57 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-alpine` - unknown; unknown

```console
$ docker pull node@sha256:33f460da10fd216f7ad0a099d0ceb834d9bec892803126d8e076128c042518b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.7 KB (413653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15e7186e6a48c3fb92627de4acf654b5b2cc823d03260c115ad65b735d2b192`

```dockerfile
```

-	Layers:
	-	`sha256:64de24a60e9ca722b1e3e3ae4a5538807e21a790ff83b5fc24a2ca745cf8f337`  
		Last Modified: Tue, 07 Jan 2025 09:08:58 GMT  
		Size: 388.3 KB (388333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:079d9dccbc6d638aeddd54cc4af0973358c040c545732da2e80e601979e263b1`  
		Last Modified: Tue, 07 Jan 2025 09:08:57 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

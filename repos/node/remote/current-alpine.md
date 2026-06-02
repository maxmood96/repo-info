## `node:current-alpine`

```console
$ docker pull node@sha256:8b060a63f66cebebb3644abdcd9f55a793c6dbf5a15f214e0487647da09f0a9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:current-alpine` - linux; amd64

```console
$ docker pull node@sha256:6f3a342603870772338e02ac93a9248520884db7abe194917f1219628c632b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62559794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5165330357caa120c9264311a496304948cc1d89d5189d9ac2648426ec4ddcbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 01 Jun 2026 22:46:00 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:46:00 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="804631aecd25cef5252ac52bc138647c495a87f8597dccd336faf1437d32709b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools         rust         cargo     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:46:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:46:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:46:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155e0e3178a764eb9b2f96c5af499da7118aa5699139637c233dd0d8f18469ba`  
		Last Modified: Mon, 01 Jun 2026 22:46:16 GMT  
		Size: 58.7 MB (58695152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6fc0b1ba74aa1383992762af9bbbf67e9deb8530dd4ff76ecc11aa18a787f1`  
		Last Modified: Mon, 01 Jun 2026 22:46:14 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-alpine` - unknown; unknown

```console
$ docker pull node@sha256:75a389e2446eee337db15a7cb901c86e5fc3e9f6b6ba07ef6692891890d7a868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 KB (315168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d015c56fc0fd19dbd52a08a960fed5f385b705ab11fb79894e046dbbfe6083`

```dockerfile
```

-	Layers:
	-	`sha256:bc867ea0d23e7d72c2f7318ccd13d21975a635cf223bd6cda71067d099b1dc75`  
		Last Modified: Mon, 01 Jun 2026 22:46:14 GMT  
		Size: 294.3 KB (294258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2872bbf408301061440f80c03375fe1d17f1a314299f8945b62d5f8e0ee75f31`  
		Last Modified: Mon, 01 Jun 2026 22:46:14 GMT  
		Size: 20.9 KB (20910 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-alpine` - linux; arm64 variant v8

```console
$ docker pull node@sha256:b89760c2686355fb59b39e5a74c290ff7fe69c38d2a159ca7923b047a332ba0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63544953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75dee730b7244603f29812d37ad71fc05bc7a796294788825a1d2a2efb27fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 21:01:03 GMT
ENV NODE_VERSION=26.2.0
# Wed, 20 May 2026 21:01:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3224ba9c6ae722120971e9424a6c2e0552c8b6ce89cf9dcc36e17485d661aff7" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools         rust         cargo     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 20 May 2026 21:01:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 21:01:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 21:01:03 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c867d4cffab255fab6e2bd7174f37f558bc1d3d4df191e9500bd6530390d21`  
		Last Modified: Wed, 20 May 2026 21:01:21 GMT  
		Size: 59.3 MB (59344638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00c978db8f8b55ce4170fce778535ee7b3edd06dad44addf3a24bdb97a38e8f`  
		Last Modified: Wed, 20 May 2026 21:01:19 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-alpine` - unknown; unknown

```console
$ docker pull node@sha256:3d5ef732de4410ffe1f97a899d201a4b022e52403fef8dd4ae5a2d5128396267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 KB (314820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c6e040cade2248f9132e8758e343864d8e2902e988f6990b5054be00e36d60`

```dockerfile
```

-	Layers:
	-	`sha256:a65260c9f9758d6755d84c7cac2e8e415edba0ce6d251fc64f8f0feaf163a0bd`  
		Last Modified: Wed, 20 May 2026 21:01:27 GMT  
		Size: 293.7 KB (293734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:659599cd9c27e9b720aead95acfc28b6813e0dfa87f351de27a934aa949063db`  
		Last Modified: Wed, 20 May 2026 21:01:18 GMT  
		Size: 21.1 KB (21086 bytes)  
		MIME: application/vnd.in-toto+json

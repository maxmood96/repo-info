## `node:26-alpine3.24`

```console
$ docker pull node@sha256:9c0e1e52125d6b67d505cf75b4880fcf1290ccea5c480849910e1d57b2cf72b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:26-alpine3.24` - linux; amd64

```console
$ docker pull node@sha256:6e24acff8a03e79cdae25716a1580afdaf6fdd8218874d7073f15007f1c1f95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62542111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df611fee17ba6f20093d34fb9d585b928a387d89b083ddead7fbbea5bd0dc438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:19:50 GMT
ENV NODE_VERSION=26.3.0
# Tue, 16 Jun 2026 00:19:50 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="804631aecd25cef5252ac52bc138647c495a87f8597dccd336faf1437d32709b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools         rust         cargo     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Tue, 16 Jun 2026 00:19:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:19:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:19:50 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b4e35e4670716fd40a076727f235cf8eb5ba07d9d76a4a9e266fa0ece630f0`  
		Last Modified: Tue, 16 Jun 2026 00:20:06 GMT  
		Size: 58.7 MB (58695268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c28a690ae8b95dac78108c12948cd058d4bcc8b7b813741c9761fca2623ad4`  
		Last Modified: Tue, 16 Jun 2026 00:20:04 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:26-alpine3.24` - unknown; unknown

```console
$ docker pull node@sha256:abc09efc89749ef085904b76bbef6addad5c869c9264ae837ffd12c9f4bbcf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 KB (315164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bf0abc47587369c7310885d732c7d8f7f76df81a17360a710f36ec02b3a63c`

```dockerfile
```

-	Layers:
	-	`sha256:a197b8a707eb91e048f55c72c53d04d615b7c945a583c1b40b8c42deb612e347`  
		Last Modified: Tue, 16 Jun 2026 00:20:04 GMT  
		Size: 294.3 KB (294254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2497c880ea5811e4c8aa849e1301d149f804a6f26db06e8e84e541bfcec0e55d`  
		Last Modified: Tue, 16 Jun 2026 00:20:04 GMT  
		Size: 20.9 KB (20910 bytes)  
		MIME: application/vnd.in-toto+json

### `node:26-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull node@sha256:0ac002a504e882cd36a71d90c9885b21365539bc9d053afbc2f951b26c6e74a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63498425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378a88c42b3ec728daa02e0be2802467d8636b444e469fa8055c60a61025b5d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 01:06:42 GMT
ENV NODE_VERSION=26.3.0
# Tue, 16 Jun 2026 01:06:42 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="804631aecd25cef5252ac52bc138647c495a87f8597dccd336faf1437d32709b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools         rust         cargo     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Tue, 16 Jun 2026 01:06:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 01:06:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 01:06:42 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03db348347b6c0b6f32860e225e7b91e8e0e49974d4b24e4a504f0fb8c00795`  
		Last Modified: Tue, 16 Jun 2026 01:06:59 GMT  
		Size: 59.3 MB (59314942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5e1b68fb11c11b909110060313d30f03ebf29a8dfa9a8e30e896df6277f971`  
		Last Modified: Tue, 16 Jun 2026 01:06:57 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:26-alpine3.24` - unknown; unknown

```console
$ docker pull node@sha256:ad0177a9e914a3666c488078e8663ea84ea22e349f98ec50649cb90948529a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 KB (314818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4292b9a532bb0afb8e4dd2f284db4125c9bb1904eca60237f25cfbe8f75f9403`

```dockerfile
```

-	Layers:
	-	`sha256:c0201a18240bbed5ff0988afb1dc7f02da7ef51cee7c1ba9a8714c5c2761aeef`  
		Last Modified: Tue, 16 Jun 2026 01:06:57 GMT  
		Size: 293.7 KB (293732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:728eef2ad3705e242eb06d23f0082319596765a054fe0f56e90d2068874c4481`  
		Last Modified: Tue, 16 Jun 2026 01:06:57 GMT  
		Size: 21.1 KB (21086 bytes)  
		MIME: application/vnd.in-toto+json

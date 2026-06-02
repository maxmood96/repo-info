## `node:26-alpine3.22`

```console
$ docker pull node@sha256:0fac83b55183b88746fde518159c956c81e14f3530fdacda7ba01b9c9e882743
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:26-alpine3.22` - linux; amd64

```console
$ docker pull node@sha256:ec97bb585eb1ac122fc3783150adab10cd79baab7c2ce0aa0b03622d233fbe7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62478967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6927b8eb124e838a569b18c453a4d573129b3d03e38bdff5761fce8427f06542`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Mon, 01 Jun 2026 22:45:56 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:45:56 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="804631aecd25cef5252ac52bc138647c495a87f8597dccd336faf1437d32709b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools         rust         cargo     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:45:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:45:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:45:56 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66ba5ab6ce6123b38ff843684b1c4e8e4b1c6801fd1a3db4cca25d9ab27e704`  
		Last Modified: Mon, 01 Jun 2026 22:46:12 GMT  
		Size: 58.7 MB (58670326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e275868400edeb24a857647e56b6924f286a2993d0b7282fc35aa4809841b79`  
		Last Modified: Mon, 01 Jun 2026 22:46:10 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:26-alpine3.22` - unknown; unknown

```console
$ docker pull node@sha256:6985f42fab556a5cadb14ba4400d7cafe206105baf9a9bc0e22907e4b51ddef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 KB (313415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e77597ce63ca6748a6fbbac54361cb7a7210bd9a9e079bcebf3721184dfe10`

```dockerfile
```

-	Layers:
	-	`sha256:4e6c3d00825badfa52a63f8c06923571557ab3eda41ba8013de9e9bb60be0c67`  
		Last Modified: Mon, 01 Jun 2026 22:46:10 GMT  
		Size: 294.0 KB (294021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07fd27572c0945c654e584544e49c0e61fa26c3ef7c1a262becb2051e7228732`  
		Last Modified: Mon, 01 Jun 2026 22:46:10 GMT  
		Size: 19.4 KB (19394 bytes)  
		MIME: application/vnd.in-toto+json

### `node:26-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull node@sha256:2812bc318e5f0cba0c6b6ddc220bc70badda44e81096f7740798338b8f1328b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61878460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8954f5aacbc8cdd414a3a4812c6cf39a27789610dc175f0da5f334683c378b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 21:23:52 GMT
ENV NODE_VERSION=26.2.0
# Wed, 20 May 2026 21:23:52 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3224ba9c6ae722120971e9424a6c2e0552c8b6ce89cf9dcc36e17485d661aff7" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools         rust         cargo     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 20 May 2026 21:23:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 21:23:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 21:23:52 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adb4a69f700e279873815ba7e4ee92345660999a27fc6b7e9eb0f0ca07ff86e`  
		Last Modified: Wed, 20 May 2026 21:24:10 GMT  
		Size: 57.7 MB (57736120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c9ed4b76a7ca06d5b21d633b1ba2d826ca9b073f3676ff3fb8b7dadd5cb2aa`  
		Last Modified: Wed, 20 May 2026 21:24:08 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:26-alpine3.22` - unknown; unknown

```console
$ docker pull node@sha256:0d8557c150fff52918323eb3946faccdb61cbfc04be195abaa2a722c7f5b4a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 KB (313597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53478e62d2a0dfe13dfc20587d529144e429a60e85aeabb6163ed8289a8caf0c`

```dockerfile
```

-	Layers:
	-	`sha256:b189bb4cf52e7e5f47d21ab1f7523a1c6183e4fa22980ff5fe7a5c67c07fddca`  
		Last Modified: Wed, 20 May 2026 21:24:08 GMT  
		Size: 294.1 KB (294087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b064a0eb00276e3b2c25a05d09c36a99ad495b36645068fd13254b7c32b4615f`  
		Last Modified: Wed, 20 May 2026 21:24:08 GMT  
		Size: 19.5 KB (19510 bytes)  
		MIME: application/vnd.in-toto+json

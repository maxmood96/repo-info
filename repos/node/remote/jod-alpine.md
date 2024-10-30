## `node:jod-alpine`

```console
$ docker pull node@sha256:58508134c58ba08106c9edcacc062061ee867f9e1389ef3e3f630e720a0b988e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `node:jod-alpine` - linux; amd64

```console
$ docker pull node@sha256:6fdb5a2cf4f4727c3ec873177330a984caf5c0851ec4bd80ef55da7f634c7722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54247317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8847cc4ac5ca55b993ebcc0cd7b994c5e083a606eef81cf4cdb4126169c1d2c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 20:39:22 GMT
ENV NODE_VERSION=22.11.0
# Tue, 29 Oct 2024 20:39:22 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="95e9a410b7ce732705493cd44496c8e77ccb11516c75c2ef794f19a9943d178c" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
ENV YARN_VERSION=1.22.22
# Tue, 29 Oct 2024 20:39:22 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 20:39:22 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f037f8beafdb35ef5c9a7254780c75e81cf3b2505ab9f8be06edc4a6eca4dbec`  
		Last Modified: Tue, 29 Oct 2024 21:57:42 GMT  
		Size: 49.2 MB (49236789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e96017b105b9b791db5b1e1a924abdd3d066861fa8c5c29e4b83dbbea2c8b2d`  
		Last Modified: Tue, 29 Oct 2024 21:57:42 GMT  
		Size: 1.4 MB (1386275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9c86674f9fdc9f31743b0ceb6769531a0a5d4d9d0b8fb1406f03f92d72c4b4`  
		Last Modified: Tue, 29 Oct 2024 21:57:41 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:jod-alpine` - unknown; unknown

```console
$ docker pull node@sha256:35e8f506f9ba5639f6ad38dca5a5fdb979848b9a9100f6d55d63731332890ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.3 KB (438349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752fcb97bf975bb548c7057b3494a332e94ce6f46bc4827c7b5133c0a3b57a38`

```dockerfile
```

-	Layers:
	-	`sha256:274078e577680477a2b08d28340115761f5fb1eb4e4fb73d44ce60cb1072dc66`  
		Last Modified: Tue, 29 Oct 2024 21:57:42 GMT  
		Size: 413.2 KB (413219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8a2a43a13f75d5fa28a429f556de89bdfb6c039846dceacaa42b74961a823f`  
		Last Modified: Tue, 29 Oct 2024 21:57:41 GMT  
		Size: 25.1 KB (25130 bytes)  
		MIME: application/vnd.in-toto+json

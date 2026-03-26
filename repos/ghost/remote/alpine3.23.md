## `ghost:alpine3.23`

```console
$ docker pull ghost@sha256:62118333c1b350bbc8a79b66a501872589d879041080648362d838e8087def46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:17e03325d58ff718e601243888439c463c3ff36cd87e1a2d3febb8562e86ecc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226138872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5ece86ae1d2cd1e1dfe81f5cd9f88183213bf1106f3fd382b0df9654ebd00d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 26 Mar 2026 05:36:19 GMT
ENV NODE_VERSION=22.22.2
# Thu, 26 Mar 2026 05:36:19 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 26 Mar 2026 05:36:19 GMT
ENV YARN_VERSION=1.22.22
# Thu, 26 Mar 2026 05:36:22 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 26 Mar 2026 05:36:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Mar 2026 05:36:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Mar 2026 05:36:23 GMT
CMD ["node"]
# Thu, 26 Mar 2026 06:10:04 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 26 Mar 2026 06:10:07 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Mar 2026 06:10:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Mar 2026 06:10:07 GMT
ENV NODE_ENV=production
# Thu, 26 Mar 2026 06:10:07 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Thu, 26 Mar 2026 06:10:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 26 Mar 2026 06:10:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 26 Mar 2026 06:10:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 26 Mar 2026 06:10:16 GMT
ENV GHOST_VERSION=6.22.1
# Thu, 26 Mar 2026 06:12:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 26 Mar 2026 06:12:26 GMT
WORKDIR /var/lib/ghost
# Thu, 26 Mar 2026 06:12:26 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 26 Mar 2026 06:12:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Mar 2026 06:12:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Mar 2026 06:12:26 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 26 Mar 2026 06:12:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac107224afb008bb83b20444cbc051b129c0ccd8b8db1f42662ab3c42eb0000`  
		Last Modified: Thu, 26 Mar 2026 05:36:36 GMT  
		Size: 52.0 MB (51962304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fd9b73af2598c327c66de0de2e9ebe61c85bb1924fcfdf77b80055161a4b84`  
		Last Modified: Thu, 26 Mar 2026 05:36:35 GMT  
		Size: 1.3 MB (1262115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087b41e5c641ca5ca6e39de79290a61a4f50b3b3a5fbe7db44a0f05c103a6275`  
		Last Modified: Thu, 26 Mar 2026 05:36:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260a434ab61b6718a14f963653de3afb4b4a3054e4cc343d0694b8d7efa154de`  
		Last Modified: Thu, 26 Mar 2026 06:13:04 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166fec1a6e33e5181310866c5f5c0efc1ca194ed669f3e5f782b344e9bb7a12d`  
		Last Modified: Thu, 26 Mar 2026 06:13:04 GMT  
		Size: 928.3 KB (928318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0120f1cc26ec76aa9ddb61bcd43841078f3d944bc2a65e35cfc80d99dad633f4`  
		Last Modified: Thu, 26 Mar 2026 06:13:04 GMT  
		Size: 13.6 MB (13629268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4b5f8056628f271356beef218b64eb40b054cd87c79ba1e471e2027d674a80`  
		Last Modified: Thu, 26 Mar 2026 06:13:08 GMT  
		Size: 153.7 MB (153672131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcc17ab9451dd5d3d01a370fb73aa183d5d60a351b90723bc5395d3c2a0e17d`  
		Last Modified: Thu, 26 Mar 2026 06:13:05 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:19369a159bb09498546f880dd57f704ce7364e1e85f470e0a004ebe6156f1447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3526274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645fa65ef29dd0e3c4efc3d3f7bd30d2fcfa583cfccd81fc38981b00268d0fbc`

```dockerfile
```

-	Layers:
	-	`sha256:ee87cda03659031ae23c413b11277de39b102a2f05aced152098157355ebea74`  
		Last Modified: Thu, 26 Mar 2026 06:13:04 GMT  
		Size: 3.5 MB (3499889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c67f1ec804d0b280fc773900c54c89752a6b23e814a6be39eecfe0b646c8dd6b`  
		Last Modified: Thu, 26 Mar 2026 06:13:03 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:ea3ff51dd6ec7d682299cc1ab2064475e5ae3dc47ef2261b02086a329ebe4b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238259440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0ba4357f353b2675b6849394024ca4eccfeea491ba797c06c2d5a883d0201b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 26 Mar 2026 06:06:50 GMT
ENV NODE_VERSION=22.22.2
# Thu, 26 Mar 2026 06:06:50 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c58109c8da448196f0d811df7a6079748678132067e3b53d01c8c8a4bcd86992" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 26 Mar 2026 06:06:50 GMT
ENV YARN_VERSION=1.22.22
# Thu, 26 Mar 2026 06:06:54 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 26 Mar 2026 06:06:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Mar 2026 06:06:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Mar 2026 06:06:54 GMT
CMD ["node"]
# Thu, 26 Mar 2026 06:30:08 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 26 Mar 2026 06:30:11 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Mar 2026 06:30:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Mar 2026 06:30:11 GMT
ENV NODE_ENV=production
# Thu, 26 Mar 2026 06:30:11 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Thu, 26 Mar 2026 06:30:22 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 26 Mar 2026 06:30:22 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 26 Mar 2026 06:30:22 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 26 Mar 2026 06:30:22 GMT
ENV GHOST_VERSION=6.22.1
# Thu, 26 Mar 2026 06:33:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 26 Mar 2026 06:33:15 GMT
WORKDIR /var/lib/ghost
# Thu, 26 Mar 2026 06:33:15 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 26 Mar 2026 06:33:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Mar 2026 06:33:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Mar 2026 06:33:15 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 26 Mar 2026 06:33:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5ecd9fcf87e5cc94d96ec6479d5c4f8052098922a08d59c87d561c51ef2c5`  
		Last Modified: Thu, 26 Mar 2026 06:07:11 GMT  
		Size: 52.6 MB (52585908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51669f1c95fb0aaeb584c9e379d230a1394ef361eea198a42d581674dd5052bf`  
		Last Modified: Thu, 26 Mar 2026 06:07:10 GMT  
		Size: 1.3 MB (1262985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b942d2decc49e439c5f7130350a19a2e6cc2dddf23e59896733f45e3c1c93c5c`  
		Last Modified: Thu, 26 Mar 2026 06:07:10 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163677b1f3b4c96fef702e0113ff658c710a3b5562f4b9f191e150ae58dbae5b`  
		Last Modified: Thu, 26 Mar 2026 06:33:59 GMT  
		Size: 891.3 KB (891299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5afb778320ac338c96183bb3cab7ccfa35f32d8d58f44b11ef2f067f5a1f17b`  
		Last Modified: Thu, 26 Mar 2026 06:33:59 GMT  
		Size: 881.3 KB (881271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953bdb6e99e5ef83e1d2f67ee578543a3d656ee6bf69e430d3f4f1c8eef2b581`  
		Last Modified: Thu, 26 Mar 2026 06:34:00 GMT  
		Size: 13.6 MB (13628732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971543cfe98825d1ecf6864ddd9ea385e93550f4ca906592d0abe5c8403d1cf0`  
		Last Modified: Thu, 26 Mar 2026 06:34:03 GMT  
		Size: 164.8 MB (164811141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a207ac5ce31e957288c7467e41b056e1d44893675f194232ffab53336509d393`  
		Last Modified: Thu, 26 Mar 2026 06:34:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:712e2a73ccfacace6022b72d3f556f4bf81f2cbe62472a46331860f3c73618ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3525977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2ecdcee467bc55836d0912453d8d19314bf2f88c297c3d1f1dc04b3cef0f9`

```dockerfile
```

-	Layers:
	-	`sha256:2ebd279a379505443227270154ba16ced46714f47d6879a7dbb93b1d681e3651`  
		Last Modified: Thu, 26 Mar 2026 06:33:59 GMT  
		Size: 3.5 MB (3499395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5d8e0485b0198b08b8888ed7081498106ff1216d1f4d98f6bacf63f62969b01`  
		Last Modified: Thu, 26 Mar 2026 06:33:59 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine3.23`

```console
$ docker pull ghost@sha256:45a46b522ba1a35201183889c769547927c5c77b2afc41caedc72a389fdd8645
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:3792c10914261b4a8214008600fa9852e4dd751be366dfb734bc0f5b404370b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237216008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108e18d4e5fa4e256ad95e6f3f88775bce3c303d7864ac69f15ca971577a54f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 16:56:40 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 16:56:40 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="fc04ab27123cb34d2bca3416493e86ced2f81e1ab9b51e532721ed27a1ef677d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:56:40 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 16:56:44 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 16:56:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 16:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 16:56:44 GMT
CMD ["node"]
# Thu, 04 Jun 2026 17:49:17 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 04 Jun 2026 17:49:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Jun 2026 17:49:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jun 2026 17:49:19 GMT
ENV NODE_ENV=production
# Thu, 04 Jun 2026 17:49:19 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 04 Jun 2026 17:49:27 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 04 Jun 2026 17:49:27 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 04 Jun 2026 17:49:27 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 04 Jun 2026 17:49:27 GMT
ENV GHOST_VERSION=6.44.0
# Thu, 04 Jun 2026 17:49:47 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 04 Jun 2026 17:49:48 GMT
WORKDIR /var/lib/ghost
# Thu, 04 Jun 2026 17:49:48 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 04 Jun 2026 17:49:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 17:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 17:49:48 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 04 Jun 2026 17:49:48 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad77fb7cfd3ef9f6a6dfce0020766303fd6404c57ec5d48a336265ff0201132`  
		Last Modified: Thu, 14 May 2026 16:56:58 GMT  
		Size: 52.3 MB (52314029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6816b6a041943b79e3f6e0f45fca8a0f83b376014c7525bcb108c6c7b5e9dd7`  
		Last Modified: Thu, 14 May 2026 16:56:57 GMT  
		Size: 1.3 MB (1262133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cf660f63b0ddbe3c26c27dfb34eedfbc0fd96533a1df799ee586109c18ec7d`  
		Last Modified: Thu, 14 May 2026 16:56:56 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffca4b8a5a49c8e48d87d809ddfbce65dcef9f5ca08dfcf1d00608f846de7fdf`  
		Last Modified: Thu, 04 Jun 2026 17:50:25 GMT  
		Size: 821.9 KB (821903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2b468f5fc4f013b8a8c47ade2eb345edc69315c23d18599da3c1752ffaaaf9`  
		Last Modified: Thu, 04 Jun 2026 17:50:25 GMT  
		Size: 925.2 KB (925167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cbb1a095a40314bb2e68f2cf255203d2c004e089cb534341608d20b536526f`  
		Last Modified: Thu, 04 Jun 2026 17:50:25 GMT  
		Size: 14.6 MB (14558484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e775f1baca37f0166b5f1bee0c9e482cbde69893f5a22784d388fb83a544069`  
		Last Modified: Thu, 04 Jun 2026 17:50:31 GMT  
		Size: 163.5 MB (163469077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b19bc81a0f328e92f954791f5dbdb98fef244a96dd70e087db3c39cb62f294`  
		Last Modified: Thu, 04 Jun 2026 17:50:26 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:539afeea699f616776ea6b19ac6c551b20231ecc2c582babeb2db7380c76bbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3411424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a4e716defdea0d1d882ab68810d35eef1e82b5cfc2756165e0b1b145909fb9`

```dockerfile
```

-	Layers:
	-	`sha256:dabd54f0a2ad0fcf54dd9164969192a59a599a993f6bab13fddb472a0e95b4a7`  
		Last Modified: Thu, 04 Jun 2026 17:50:25 GMT  
		Size: 3.4 MB (3384863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f27abee37c8867c3d14e84096e10001b90042f2a7c2d98cc4f1c1b695059bdb3`  
		Last Modified: Thu, 04 Jun 2026 17:50:24 GMT  
		Size: 26.6 KB (26561 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:37b88dfaed54990c2f8b7656beb90178efd0664b609c127c309aea29f0b77f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.0 MB (238036625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce41b7494d04bb21906d965cdb8b7f1cdeb32ae43f12e11281c95e47b90bd5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 17:29:11 GMT
ENV NODE_VERSION=22.22.3
# Thu, 14 May 2026 17:29:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="fc04ab27123cb34d2bca3416493e86ced2f81e1ab9b51e532721ed27a1ef677d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 17:29:11 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 May 2026 17:29:15 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 May 2026 17:29:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 17:29:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 17:29:15 GMT
CMD ["node"]
# Thu, 04 Jun 2026 17:49:16 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 04 Jun 2026 17:49:18 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Jun 2026 17:49:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jun 2026 17:49:18 GMT
ENV NODE_ENV=production
# Thu, 04 Jun 2026 17:49:18 GMT
ENV GHOST_CLI_VERSION=1.29.3
# Thu, 04 Jun 2026 17:49:29 GMT
RUN set -eux; 	corepack enable; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 04 Jun 2026 17:49:29 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 04 Jun 2026 17:49:29 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 04 Jun 2026 17:49:29 GMT
ENV GHOST_VERSION=6.44.0
# Thu, 04 Jun 2026 17:49:52 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node pnpm store prune; 	gosu node npm cache clean --force; 	npm cache clean --force; 		cd current; 	gosu node node -e 'require("sqlite3"); if (!require("@tryghost/image-transform").canTransformFiles()) throw new Error("sharp not installed");' # buildkit
# Thu, 04 Jun 2026 17:49:53 GMT
WORKDIR /var/lib/ghost
# Thu, 04 Jun 2026 17:49:53 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 04 Jun 2026 17:49:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 17:49:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jun 2026 17:49:53 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 04 Jun 2026 17:49:53 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d608f48b26f54edd7120a9b1cf8599d4b2a582c63819978e42ed2bd859f7f52`  
		Last Modified: Thu, 14 May 2026 17:29:32 GMT  
		Size: 52.7 MB (52665717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb91a13b2dbfd4b2a19e6e389616562c085b869987f1ada1f45813dcf0f38255`  
		Last Modified: Thu, 14 May 2026 17:29:30 GMT  
		Size: 1.3 MB (1262996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b13dbc8524aa57a005ed0f5610a4a41934fcc551fd33fba10cc960691441ff0`  
		Last Modified: Thu, 14 May 2026 17:29:30 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b890476ce14951b6bc94ecf97e25052abc6b3fa414f207efc12e0c015c7d187a`  
		Last Modified: Thu, 04 Jun 2026 17:50:40 GMT  
		Size: 891.3 KB (891292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007141aa4ed99fcd3d6cba4a0e28461adcbc7cc9c732ea6c4317673f9ff1dfca`  
		Last Modified: Thu, 04 Jun 2026 17:50:40 GMT  
		Size: 879.2 KB (879236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a137bb63cd17c36ad242e67ec59286bb518a509caa8acfdc26c6db97988cd9`  
		Last Modified: Thu, 04 Jun 2026 17:50:41 GMT  
		Size: 14.6 MB (14562383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9ebf228604cc59644df3c5ca792f2915d9eec052300d89dd47b6a707ad5d10`  
		Last Modified: Thu, 04 Jun 2026 17:50:44 GMT  
		Size: 163.6 MB (163574114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c1fab7b50456a93c4062ec1636194cc9ae1599576777941f6e5b77ff1c8e3a`  
		Last Modified: Thu, 04 Jun 2026 17:50:42 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:03cfa1b6917077bc1bd15245a674c174cbc6709a4ebcf5c1f1f8cebc0157f6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3411105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b8a84d73b72a8eaa9c27c4f653f16511e12445801d4f1e23f0e04a5ef8a486`

```dockerfile
```

-	Layers:
	-	`sha256:4b2c3f47168fdb8e25afd6e7d365c6d72437a1e90e0f892186c77c6c4e2595ce`  
		Last Modified: Thu, 04 Jun 2026 17:50:40 GMT  
		Size: 3.4 MB (3384347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93e0245342b6bc3e6fab8484f3e10df19d28ce754cb7b28d9b396b79eaac04c7`  
		Last Modified: Thu, 04 Jun 2026 17:50:40 GMT  
		Size: 26.8 KB (26758 bytes)  
		MIME: application/vnd.in-toto+json

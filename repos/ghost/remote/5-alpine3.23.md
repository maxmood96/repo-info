## `ghost:5-alpine3.23`

```console
$ docker pull ghost@sha256:719eabb305e90bdc5a808d05fe3a28e9007c6a961157e7b4d47e1223dcb11f8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:bd0478a67e46abb08644fefb48e4e923ae21d1608f968742295feb7bc73b22dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175604403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5fdafaf380537b27a727bf096ea76eaf196fd8a30865978269e645b0e93334`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:42 GMT
ENV NODE_VERSION=20.19.6
# Thu, 18 Dec 2025 00:39:42 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a371d92fafee1b20ede35c3df747ca1c8b25fcb2e14d3a4c36b41166faae707f" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Dec 2025 00:39:42 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Dec 2025 00:39:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Dec 2025 00:39:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:39:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:45 GMT
CMD ["node"]
# Thu, 18 Dec 2025 01:23:59 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Dec 2025 01:24:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 01:24:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 01:24:02 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Thu, 18 Dec 2025 01:24:02 GMT
ENV NODE_ENV=production
# Thu, 18 Dec 2025 01:24:02 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Thu, 18 Dec 2025 01:24:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Dec 2025 01:24:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Dec 2025 01:24:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Dec 2025 01:24:12 GMT
ENV GHOST_VERSION=5.130.5
# Thu, 18 Dec 2025 01:25:03 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 18 Dec 2025 01:25:03 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Dec 2025 01:25:03 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Dec 2025 01:25:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:25:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:25:03 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Dec 2025 01:25:03 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d06ba6946d1f299d8f962e37906c77006df33d47050430a57f7893ec35af697`  
		Last Modified: Thu, 18 Dec 2025 00:40:07 GMT  
		Size: 42.8 MB (42781004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3325e64457574e24f92246e3da3376946e473d636209e1390eac47b50b26a3`  
		Last Modified: Thu, 18 Dec 2025 00:40:02 GMT  
		Size: 1.3 MB (1262118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1849a5c548bc65ee47a64498951bda5d40e87d08efe9dca69b5c8cdedc7a52`  
		Last Modified: Thu, 18 Dec 2025 00:40:02 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44897dade065e5a3c93d78799afd42092c70b413d9a174790885d82c7e99d373`  
		Last Modified: Thu, 18 Dec 2025 01:25:40 GMT  
		Size: 821.9 KB (821889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f936f03292b6cdd70145687479d2fc0015d769a6bc0d775f85b5c5f70c187f4`  
		Last Modified: Thu, 18 Dec 2025 01:25:40 GMT  
		Size: 928.3 KB (928309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5061c34ce937c0a9ef4cdac18a47aff7535da1b50bf4c9f657451a7db668a76`  
		Last Modified: Thu, 18 Dec 2025 01:25:39 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d7056ffddeb6bd6908ac634437f8f67c855ac4da18bb4234e40cbb3131532e`  
		Last Modified: Thu, 18 Dec 2025 01:25:40 GMT  
		Size: 11.0 MB (11045899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016727ad344de75a34672c99351be922566549d938694f256e15c3ab91cb3387`  
		Last Modified: Thu, 18 Dec 2025 01:25:51 GMT  
		Size: 114.9 MB (114903892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc8f6561d8e127ce7cd4da71f0b804af70b70960bccb68103ee78b4ac032e2a`  
		Last Modified: Thu, 18 Dec 2025 01:25:40 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:ce0df80a1cbcdd9ce2285dc0079a440fda44471c1a9c013f789890d1ee3feb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3361556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca01395903847ec084eb8d341b67e07f90ad43059cfcf5ecece0931ce420d370`

```dockerfile
```

-	Layers:
	-	`sha256:70c44fcb11bc153dea609bb5d026c6dad7732c6764cf26868de3192ec693ddce`  
		Last Modified: Thu, 18 Dec 2025 04:45:24 GMT  
		Size: 3.3 MB (3333261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ef7ad21de188a6b8e2685a7d71fb751f7e89cc3df8e1878c6a097b63c9a2aa8`  
		Last Modified: Thu, 18 Dec 2025 04:45:25 GMT  
		Size: 28.3 KB (28295 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:4270fa5b8017b3792f765ae02a5513f09932c3d4b434108126a9aaecdcf1ff73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186820402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763efa6b8d7439cbaef4ee60ffdb3fdca316708bfe9d2be8a394384249a8042e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:00:35 GMT
ENV NODE_VERSION=20.19.6
# Thu, 18 Dec 2025 01:00:35 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a371d92fafee1b20ede35c3df747ca1c8b25fcb2e14d3a4c36b41166faae707f" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Dec 2025 01:00:35 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Dec 2025 01:00:38 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Dec 2025 01:00:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:00:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:00:38 GMT
CMD ["node"]
# Thu, 18 Dec 2025 01:33:36 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 18 Dec 2025 01:33:39 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 01:33:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 01:33:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Thu, 18 Dec 2025 01:33:39 GMT
ENV NODE_ENV=production
# Thu, 18 Dec 2025 01:33:39 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Thu, 18 Dec 2025 01:33:56 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 18 Dec 2025 01:33:56 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 18 Dec 2025 01:33:56 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 18 Dec 2025 01:33:56 GMT
ENV GHOST_VERSION=5.130.5
# Thu, 18 Dec 2025 01:35:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 18 Dec 2025 01:35:14 GMT
WORKDIR /var/lib/ghost
# Thu, 18 Dec 2025 01:35:14 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 18 Dec 2025 01:35:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:35:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:35:14 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 18 Dec 2025 01:35:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9824d7990580162dd96cf3c8e08c9e966ed8d819adbb6e065c3c5ab73d74b4`  
		Last Modified: Thu, 18 Dec 2025 01:01:03 GMT  
		Size: 43.1 MB (43116229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9f6f8b202047f37f5d51a1f2e731b60925a601fe4c9c1495e6c000ddd25944`  
		Last Modified: Thu, 18 Dec 2025 01:00:58 GMT  
		Size: 1.3 MB (1262980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70268380327fbc2d9c066979d554cdff4c22f752e9be70bde123ec5ccb64c292`  
		Last Modified: Thu, 18 Dec 2025 01:00:58 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d895b6f5440563ac67c45ca2946dbd53c50d537b87e7dc9847872bc9e27d22`  
		Last Modified: Thu, 18 Dec 2025 01:35:58 GMT  
		Size: 891.3 KB (891292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d3dc3402c4b59eba5ae4067be198d6eae2c38e31ade6f218241ed0158fbfb5`  
		Last Modified: Thu, 18 Dec 2025 01:35:58 GMT  
		Size: 881.3 KB (881263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdefdc1d22d3e6ab90af33b24fb7d8e3dd35c62b09e1fd9bfb914da513e8c4c5`  
		Last Modified: Thu, 18 Dec 2025 01:35:58 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2641b59831ec0d63808a7e563fc61954fb7845e8373702a8068285ae5a20c65`  
		Last Modified: Thu, 18 Dec 2025 01:36:04 GMT  
		Size: 11.1 MB (11052873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8590f13342e92f36695a5141f133daf8bf1955a123e84fa9d6d33423e8dff57d`  
		Last Modified: Thu, 18 Dec 2025 01:36:11 GMT  
		Size: 125.4 MB (125418842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53caebc666a99e2b05f2c8bf902b239b341510a111451fbbeed396b0c48520e4`  
		Last Modified: Thu, 18 Dec 2025 01:35:58 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:f06fa86a4a9909f8beb3e52c9da6c346244d91d2e7a9e9f1e63936a636055f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3361226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51fd4501d09a27d4d30136188b4fd9256e32ddc384ece95d62ac455962d2d71`

```dockerfile
```

-	Layers:
	-	`sha256:188e7b9e8cd2763df74eeb8bbd82d5726e513b44a730e90abaa324eeee32fcf0`  
		Last Modified: Thu, 18 Dec 2025 04:45:30 GMT  
		Size: 3.3 MB (3332743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceaebe710b785df269868e259bbd8e062c78e76d729c9dae2310b87a80abbd95`  
		Last Modified: Thu, 18 Dec 2025 04:45:30 GMT  
		Size: 28.5 KB (28483 bytes)  
		MIME: application/vnd.in-toto+json

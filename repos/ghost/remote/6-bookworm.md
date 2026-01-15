## `ghost:6-bookworm`

```console
$ docker pull ghost@sha256:e7c95b42db9884c60a23dadeefd1472465fe874721959b430dc0d6653b343110
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:6-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:8ff4c3b99885bca14e261dbbf159250a60abd40e0bd6aa31825658b38cbc8e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229945542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d11c097664c52977c0b0263331b9de526100acd41ec9284379b93524c74f59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:57:36 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 17:59:12 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 17:59:12 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:12 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:59:23 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:59:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:59:23 GMT
CMD ["node"]
# Wed, 14 Jan 2026 22:03:01 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 22:03:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 22:03:01 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 22:03:01 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 22:03:10 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 22:03:10 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 22:03:10 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 22:03:10 GMT
ENV GHOST_VERSION=6.12.1
# Wed, 14 Jan 2026 22:05:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 22:05:07 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 22:05:07 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 22:05:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 22:05:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 22:05:07 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 22:05:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06224db79377a9070235765c986fde15b2056fe616c2808c0cea189aa52876b`  
		Last Modified: Wed, 14 Jan 2026 17:58:33 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c9adef44853b9bab15246e8900feaa9b5426d3f5a88411f0aca8a3129a2573`  
		Last Modified: Wed, 14 Jan 2026 17:59:48 GMT  
		Size: 49.5 MB (49472719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ac2b87b09265a60e104e3d87872d2c15f913cbbfd4d401b5e4b5353e4ced4`  
		Last Modified: Wed, 14 Jan 2026 17:59:48 GMT  
		Size: 1.7 MB (1712660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cc9ecead9d0fe8970f3923a484fcd4fe1fd027fab911d462ca552cd57d5dbf`  
		Last Modified: Wed, 14 Jan 2026 17:59:42 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279f9e375d730d0f016b29492229272647aba67c4fa1116b3eddbd80b9658281`  
		Last Modified: Wed, 14 Jan 2026 22:06:00 GMT  
		Size: 1.2 MB (1247514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c37e98c68d9a68fda14a184a1522855e645d129026c5e942a6215947730a000`  
		Last Modified: Wed, 14 Jan 2026 22:05:50 GMT  
		Size: 11.7 MB (11703974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637fb7af46463caf79c22a8c6d8a8b14720759fe7fa9e6960f92242beaae7442`  
		Last Modified: Wed, 14 Jan 2026 22:05:58 GMT  
		Size: 137.6 MB (137575776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d999f98f2a78b4e75c26493c954315368a7a96b63560f6737b132b6d2ae442`  
		Last Modified: Wed, 14 Jan 2026 22:05:49 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:5a489ed35f7b70c5f14b0b856e226d17b53f5133e25daefd2c708b37d9c7ab9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5619514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aaecc1aa8c925443f2fbe7cd5c8242f6b46444f11fcd1bfb6b9a067eb471e6b`

```dockerfile
```

-	Layers:
	-	`sha256:907215db90ddedc58d3153ac38cf33426d1f63b1a432c5bb991a2ce6328637a9`  
		Last Modified: Wed, 14 Jan 2026 22:46:18 GMT  
		Size: 5.6 MB (5593167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90321eee019671a2335c15141c33819f6d1b865d63363b8afbcda68b0b56acf9`  
		Last Modified: Wed, 14 Jan 2026 22:46:19 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:c7c05a8ac6906d402a1f5615c0579c08da01552052a5f90deed4da05a48f5d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221399950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7eabc1b76f8b1bab32d609fba7e6415c76ba644be69c2cc8ded57313469abc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:54:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 17:55:09 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 17:55:09 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:55:09 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:55:22 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:55:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:55:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:55:22 GMT
CMD ["node"]
# Wed, 14 Jan 2026 22:03:28 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 22:03:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 22:03:28 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 22:03:28 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 22:03:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 22:03:40 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 22:03:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 22:03:40 GMT
ENV GHOST_VERSION=6.12.1
# Wed, 14 Jan 2026 22:06:32 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 22:06:32 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 22:06:32 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 22:06:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 22:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 22:06:32 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 22:06:32 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:08 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3f69c7fd27d347a5e00644002683f0cd76f3e47a502ac1e25d3b70c6c29ca4`  
		Last Modified: Wed, 14 Jan 2026 17:55:48 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e754ab3acd6a899de6c0eb5a5237644e403af39639dca15fb24449c643906677`  
		Last Modified: Wed, 14 Jan 2026 17:55:55 GMT  
		Size: 44.2 MB (44209833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dccc1ff00c1209c0144a42a1f87752ed021e25f278e7cf001a564829028789e`  
		Last Modified: Wed, 14 Jan 2026 17:55:48 GMT  
		Size: 1.7 MB (1712838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e8bc7dcf093f62f78ede1d73b5bd230781402e1995fd741d91d58c5dc6f393`  
		Last Modified: Wed, 14 Jan 2026 17:55:48 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eaa923c0526d26cad7772e34f7d2d0e327f83c9cf3d64f49ed844f0f61a28a6`  
		Last Modified: Wed, 14 Jan 2026 22:07:19 GMT  
		Size: 1.2 MB (1214413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfc135486f9027d496d16f6ec72ab920e9af5f493ac94685fe1f9c5dfb999fe`  
		Last Modified: Wed, 14 Jan 2026 22:07:21 GMT  
		Size: 11.7 MB (11694030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f01b552891e39648891bea6b4b460d925a870b7b7c21191e8162bf529115c2`  
		Last Modified: Wed, 14 Jan 2026 22:09:40 GMT  
		Size: 138.6 MB (138630390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f42860e857f674ab9e216a0abb9668d15b613c86bf697b54e2c6b72baa5926f`  
		Last Modified: Wed, 14 Jan 2026 22:07:27 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:0801d68be77e1fc52dc9033f20ec02a31eac408560b5f56d900b01159a9b6ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5622449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a628ef65b9a838ef6519e4cdc057c4c43b95abb018f73e8cf3b4a1f81a61cf05`

```dockerfile
```

-	Layers:
	-	`sha256:b77a3dd0f6234a8eaf795940f5a828fe1b8c47fa31925b076c7fd3e2fb6c8d9c`  
		Last Modified: Wed, 14 Jan 2026 22:46:24 GMT  
		Size: 5.6 MB (5595964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c76319a4281b6fa5771bd9d56f8c5e73e29304c25105b6929b78f5764aa1eb8`  
		Last Modified: Wed, 14 Jan 2026 22:46:25 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:3235033af8d33d3580e138448733aeea3e6a6ec4e9cd51a5d02b2afb66d1a937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230009217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538d387060b46cfdb28c3601d00d719dfb9b616e164846bb8c102a62ec561505`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 18:01:04 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 18:01:22 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 18:01:22 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:01:22 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:01:34 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:01:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:01:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:01:34 GMT
CMD ["node"]
# Wed, 14 Jan 2026 22:02:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 22:02:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 22:02:47 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 22:02:47 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 22:03:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 22:03:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 22:03:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 22:03:01 GMT
ENV GHOST_VERSION=6.12.1
# Wed, 14 Jan 2026 22:05:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 22:05:26 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 22:05:26 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 22:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 22:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 22:05:26 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 22:05:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87c15c864725a8daa5ca1505d5d886e53928b49fa578e7a35dc51a4be5b715d`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4c74fb4662b26fe96702c59c427e26bd0489a0a1c1c5960592b029426583e3`  
		Last Modified: Wed, 14 Jan 2026 18:02:01 GMT  
		Size: 49.6 MB (49611029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20454c8e368d7849b8d2669b17f01d47585f0d71a5b683c0c03997c8733f81d2`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 1.7 MB (1712623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6686bd0124e3e3612ac03ec0e58e60f1d86a689763f36ecade62f90a4f8d1ea`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6267bea67193ac9e0be0928a3863c560d22e6e72c6b7b1ec75684f1febab7298`  
		Last Modified: Wed, 14 Jan 2026 22:06:13 GMT  
		Size: 1.2 MB (1201483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55107ee9f9d53254a836433b98194cbaa5dbf58cab131b2e0049f88f2f7c2266`  
		Last Modified: Wed, 14 Jan 2026 22:06:14 GMT  
		Size: 11.7 MB (11704277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171ecb37a85882fc1ea2b09d29acba151b54615e97c7fbdf20cd428c2d157c87`  
		Last Modified: Wed, 14 Jan 2026 22:06:29 GMT  
		Size: 137.7 MB (137667588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaf8a977119c8e284e0845b1cfa84aaf3d2b80d859be9ce74506eeb0032a5e5`  
		Last Modified: Wed, 14 Jan 2026 22:06:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:899784eb2e5e74b09e03435e618eeafb6610eb8b083bdf4f2f8c49ef6866ceb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5620047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b14e9b11d7eeb7d2172df0305c05c6f4fabe07ec1547de17abb339b6c79787a`

```dockerfile
```

-	Layers:
	-	`sha256:155e7a9bbb24a62b56291c97cb993ae11bf3ea990416295d0abfc60ae2c7e6de`  
		Last Modified: Wed, 14 Jan 2026 22:46:30 GMT  
		Size: 5.6 MB (5593518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fade8f95bbe8d544c4af1bed1a6d0431ed9462bed0eaeef8559856dc6b202728`  
		Last Modified: Wed, 14 Jan 2026 22:46:31 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:2f2a2b44bfd86bfc0ae03dddd3cbd9658a43d694a96d428b4d234048a032f697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231928821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef72561bd279233196564aa3a65b122aae07100fd587abb89e4e72c80f37b2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 13 Jan 2026 02:18:07 GMT
ENV NODE_VERSION=22.21.1
# Tue, 13 Jan 2026 02:18:07 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 13 Jan 2026 02:18:07 GMT
ENV YARN_VERSION=1.22.22
# Tue, 13 Jan 2026 02:18:18 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 13 Jan 2026 02:18:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:18:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:18:18 GMT
CMD ["node"]
# Tue, 13 Jan 2026 03:51:24 GMT
ENV GOSU_VERSION=1.19
# Tue, 13 Jan 2026 03:51:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 13 Jan 2026 03:51:24 GMT
ENV NODE_ENV=production
# Tue, 13 Jan 2026 03:51:24 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Tue, 13 Jan 2026 03:51:50 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 13 Jan 2026 03:51:50 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 13 Jan 2026 03:51:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 13 Jan 2026 03:51:50 GMT
ENV GHOST_VERSION=6.12.0
# Tue, 13 Jan 2026 03:54:04 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 13 Jan 2026 03:54:05 GMT
WORKDIR /var/lib/ghost
# Tue, 13 Jan 2026 03:54:05 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 13 Jan 2026 03:54:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 03:54:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 03:54:05 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 13 Jan 2026 03:54:05 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d139ad9a3a58767f140c3201036e062e1a612d605a2d9ad8f971d9d78b53105`  
		Last Modified: Tue, 13 Jan 2026 02:24:26 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b62d59b1f90cb8658026fff27a13ccb628465b5ada8e9361eb4bb239a24fdd1`  
		Last Modified: Tue, 13 Jan 2026 02:18:53 GMT  
		Size: 49.7 MB (49676917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daca16291699e7f72b1c9c8f992e67be658db86989f8b3bc72eeb74eaa8c21c`  
		Last Modified: Tue, 13 Jan 2026 02:18:48 GMT  
		Size: 1.7 MB (1712686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a065f46fbbbe3ec19b63d95dae30a14505759a0d7a770a31327cb3b5ef21f674`  
		Last Modified: Tue, 13 Jan 2026 02:18:48 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466a334139e6679d5cf23aff0c555d66c096392d637f970ecb5cc54f3280bbd4`  
		Last Modified: Tue, 13 Jan 2026 03:55:06 GMT  
		Size: 1.2 MB (1221352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5fd5bc853b84158f238af2c2f72f63d84d63b7f7f992f5be7283df6b19fb2f`  
		Last Modified: Tue, 13 Jan 2026 03:55:07 GMT  
		Size: 11.7 MB (11711739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c18d3f46ca34420f6a073bd17a59b4b7ab561dd12ecbcde07b3b6037aa8084`  
		Last Modified: Tue, 13 Jan 2026 07:50:18 GMT  
		Size: 140.7 MB (140717386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec2aa156c55397df2b3e4213a7a22f412974e75065f2dc23bb783925e4f602b`  
		Last Modified: Tue, 13 Jan 2026 03:55:06 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:b83a66c7e15cf1b9e602c52a1e9d08d63a4b04388ba08a4f63cdd5939bbab412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b7cb0bd64e3db635483821b457da5d3f1ff467c17f0e212306e659896cbd17`

```dockerfile
```

-	Layers:
	-	`sha256:ac84ea8e1e8bbbeab4546cac244803cac0846fea457b7cf2050fed9b9a1630f9`  
		Last Modified: Tue, 13 Jan 2026 04:46:40 GMT  
		Size: 5.6 MB (5586992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50d9f465e531fda417af5ee126ac8d3b6fd199c4368d40edac711ac76f042026`  
		Last Modified: Tue, 13 Jan 2026 04:46:41 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

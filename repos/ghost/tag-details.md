<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:6`](#ghost6)
-	[`ghost:6-alpine`](#ghost6-alpine)
-	[`ghost:6-alpine3.23`](#ghost6-alpine323)
-	[`ghost:6-bookworm`](#ghost6-bookworm)
-	[`ghost:6.22`](#ghost622)
-	[`ghost:6.22-alpine`](#ghost622-alpine)
-	[`ghost:6.22-alpine3.23`](#ghost622-alpine323)
-	[`ghost:6.22-bookworm`](#ghost622-bookworm)
-	[`ghost:6.22.1`](#ghost6221)
-	[`ghost:6.22.1-alpine`](#ghost6221-alpine)
-	[`ghost:6.22.1-alpine3.23`](#ghost6221-alpine323)
-	[`ghost:6.22.1-bookworm`](#ghost6221-bookworm)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:alpine3.23`](#ghostalpine323)
-	[`ghost:bookworm`](#ghostbookworm)
-	[`ghost:latest`](#ghostlatest)

## `ghost:6`

```console
$ docker pull ghost@sha256:1582ff7d419839eea2d5d75867703a6344f0df818f1b31680fe68b2c77940ea7
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

### `ghost:6` - linux; amd64

```console
$ docker pull ghost@sha256:2f9bb6d9eb2bfab9f2dfd77fdd9a821189a3b6d68f1317070ecbc3afb227e4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248679987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e570be6b9273a46c7912f31b3ae1719a8b895f687517bf63e96c538828f85387`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:26 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:56 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:56 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:56 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:56 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a57a621e2f90878c454c2900fb34b2e03bedcc306a9222c107772613672dfc9`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 1.2 MB (1247569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaa7fbb100f45ffee6750ca12ac096340c2913a360a8beeda5ba4b01d694e28`  
		Last Modified: Mon, 23 Mar 2026 21:33:38 GMT  
		Size: 13.7 MB (13681613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daadcb48818fecaf7145d281b62f72d64c73203df1b5c1cba03554f9ef67687`  
		Last Modified: Mon, 23 Mar 2026 21:33:41 GMT  
		Size: 153.8 MB (153847869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df50c7aa534128b8fa46cf0add79d4ffb8b57bbc4af16455f1339cd50731dda`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:0ea1489cab0174441d8a6e634f79e701d7a3e677c0919a594d84fc440955add4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e628c3c13542d24af4a7d4661639ed0a14f390a888b038f268dfdcf98e81fc2`

```dockerfile
```

-	Layers:
	-	`sha256:192a7f22b112d9ec1b7ef28fb42ad6fcbdd2f4687d1eaee3e28d6aa445a210f3`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 5.7 MB (5728841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d568062998c575776388d04c7090d619bb718a28c6d2f0001b4ec6e6d8a6bd`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm variant v7

```console
$ docker pull ghost@sha256:20fdc88d1557e233521af22d56acb959c23fb93c1687ca379d2de2979762415c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239965609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05013a90d878f774ed0f6cad6150f890362b5132d3dd76a36d2937df4b65ec87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:23 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:33:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:33:45 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:33:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:33:45 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:33:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9d4a88a3446ee882364a12dd45715592c8caf3941e70428d8bf80a50dc475`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 1.2 MB (1214351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66730a7e2a8e64649282d3e679b71b0794a963394be7f23532455764aaa4fac3`  
		Last Modified: Mon, 23 Mar 2026 21:34:30 GMT  
		Size: 13.7 MB (13671566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d599dc93bd69676edfb560878bfe6d869ac45745b0979d94d2aa4fb664600704`  
		Last Modified: Mon, 23 Mar 2026 21:34:33 GMT  
		Size: 154.7 MB (154747466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692414abc743d668b09fde51ab99e741deb58e289ed9f52ecfb271b5129869a`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:37f22098bff7f063d035344e295141ddd850fbedaf5a82fb1c7f24a0d448cc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5758123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8956d6025e4be66b9993790b8db707e33f9118b5022cde428d8bd8c35b1941`

```dockerfile
```

-	Layers:
	-	`sha256:09a626197c2b8838253dd647d94b0318b368f11d81cda127086788e043553976`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 5.7 MB (5731638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02b21ea1347601077dbf5d111f5fe8fd9ddeb4bf593027117a925952bfcae826`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:532df5ac9173a7ebb5a9890200818ebb00a4cd93c0d45ed5dbb11b8f7128f8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248989503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083043a4af7a3b001169fa4eb222731b19ebdbbafc21e6003b22609973e60670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:55 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:55 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8884c3f01372d2e4a7474c46a6a3f4c832daab7aa1b99822ebb911326b6420ce`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 1.2 MB (1201503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea814e0687d3f76992f290145881ac774ea1dda23513db4a31b5aaf6921c4d6`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 13.7 MB (13683347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f8618f0b7718f83c70cf3af35e1bf838e322049b898af2e5f6a6b1ae38a27e`  
		Last Modified: Mon, 23 Mar 2026 21:33:44 GMT  
		Size: 154.2 MB (154187137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b24587a07d6009c6736c1b37ccd2617dd2215278bea85ea10c28dd7ceb4d9f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:c2bddbf5e655a85a72932c684c632cbe432aa824337d46b3d5c5fbf32be2cf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77145a0f19a1617977a8e7073d6dc1b0643b9b715a13d4400fff20c584ace01`

```dockerfile
```

-	Layers:
	-	`sha256:ebfad0586565c6db9343b78119476e7c9e5d0c3abfc1eb96c805c1962b5346d4`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 5.7 MB (5729192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b6450155958226ae3645f5b860b28cf158b635f3e0218e7046a3ddacdb8be3f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; s390x

```console
$ docker pull ghost@sha256:10c95b76ee1638c2b14965868938bf3df60c5420a9c51005d92d61eaf5eec7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250552024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd62e5e5b20c5c893d64d2a0d63d8909b9c128398afc662a97ef4caab16ea690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 21:02:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 21:02:36 GMT
ENV NODE_ENV=production
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:06 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:06 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb0991be587623bd7e5d5529f267aa799aa553646701411b326cf0bedc49f08`  
		Last Modified: Fri, 20 Mar 2026 21:12:35 GMT  
		Size: 1.2 MB (1221347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb6fab34355db319427c08ce5355f0ce4a7847585df335e90fcb1501e579317`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 13.7 MB (13685080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98733d2270747b6d6976cba73d3d17322fefe55018112ba288b4617d60a4cf07`  
		Last Modified: Mon, 23 Mar 2026 21:33:09 GMT  
		Size: 156.9 MB (156906054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913dbdccceed1570268555c5dc113a437a4913eff641d7dd82c7b1f6f15976f`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:a55cf19c79761f21d1352e52d9edb2dda75bd55e2742b5dfd85703eb0502f18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1796ca6388170fe21901544915383a04e469322a542570b61fb8ea477b7d85`

```dockerfile
```

-	Layers:
	-	`sha256:97cd11b0670fff5b1f270a8d33607a18e76d5a242238ee55b75cc6ecaa9ba413`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 5.7 MB (5722666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2b1cc7ccf96fcd3b69663a88f6246e4d6fb638b7d3695a1909fd6180eeb831`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine`

```console
$ docker pull ghost@sha256:4f02907212c3a27dac837a51ace205f13d697c8e5d7ce611cbfb0e4d29551142
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:323e7dc6f9c45075623fbc7b0ab34cb4ed4833b6f4e3a4a654cb68cfc9bdc21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226302331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a12d8a5f0844d7eebaf1a0193281509a2cc5e793babb6f0ac8211a3677e90e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:51 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:15 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:15 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d61e4e317c93f7baa694fdee1e67ab024f703469c8f8e8c9260fe7967a5db`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8c827691e7d79dde0d5895995f8d82a90e4f56d368553bb000e1b8dda8c474`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 928.3 KB (928324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a0a060db6076d19c841d8a37264576eba6722afa2dabe585bee0248a8c434`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 13.7 MB (13681970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ae0207198a3255726cc8557821cfde799fae904dd24a9c36ccee160e7d2989`  
		Last Modified: Mon, 23 Mar 2026 21:32:57 GMT  
		Size: 153.7 MB (153673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d4c9cd4325f2571654f24b325523ef79773d87fb951673c703cfabf3f43aa5`  
		Last Modified: Mon, 23 Mar 2026 21:32:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:ab342386cefb634491e1d5f2506ae9fc03b9c751966a043d5f64c11f0649020a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e573160abafe3de68a1a7e2e1cc47fe0c34936749ecbca49d88a198e4431ebf`

```dockerfile
```

-	Layers:
	-	`sha256:fd8de3eb23b5baac30eec58502a79e393804c6facd7fa1c570ff4a1b63bfdeac`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 3.5 MB (3516840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea448e68e834543f49ce7ae9f41c3656ba6443a98ff48cfd359eadcb2e222fd`  
		Last Modified: Mon, 23 Mar 2026 21:32:53 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:f549dfa0f470bccc18f44ca1a2f507ecafeec4553ab93d465a8d15479a3be0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238420685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8640b018bfaaec34fa1df815b396cf927c2a82a76f28a4d17144abf7fe834b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:35 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:35 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064521911821dc19024bfe059748914160b230bbe68557dd98762deb1b6b43b6`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 891.3 KB (891302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1567db9f8b8a62a578279fda7f78fd3faccaf1d3269de769cafa7d141f80c97`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff613941cfbd284f01e4a2ba730151924641d94d1d7ea7d28a647526d47997b`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 13.7 MB (13682926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2598f4dbb9b4dbcefda013229846cea551c0c45feae80f8ec7ff020211922e`  
		Last Modified: Mon, 23 Mar 2026 21:33:24 GMT  
		Size: 164.8 MB (164807296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b879ea0c6b80ed51f2886e5ca6537a10ba26fbfd50daf9872ccb37d9bef6b0`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:5fbb4a54c0909702a7bbca920d61aa85ae8d4e32876f1e08a1a9c72edbb1f002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ef8a87c4cb31dbacba647a84c613cebfe2b32ffb09339785b694ca7a7b18fa`

```dockerfile
```

-	Layers:
	-	`sha256:2546e7cffbbfdc7c439fa4fb5505c6184fec8500270676ce9f94c6a4da52fe54`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 3.5 MB (3516346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9c9c17adf902326fb0ef26ddad508ee7c1baa23d3dc8d0cf980e7f58b71b52`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine3.23`

```console
$ docker pull ghost@sha256:4f02907212c3a27dac837a51ace205f13d697c8e5d7ce611cbfb0e4d29551142
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:323e7dc6f9c45075623fbc7b0ab34cb4ed4833b6f4e3a4a654cb68cfc9bdc21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226302331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a12d8a5f0844d7eebaf1a0193281509a2cc5e793babb6f0ac8211a3677e90e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:51 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:15 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:15 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d61e4e317c93f7baa694fdee1e67ab024f703469c8f8e8c9260fe7967a5db`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8c827691e7d79dde0d5895995f8d82a90e4f56d368553bb000e1b8dda8c474`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 928.3 KB (928324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a0a060db6076d19c841d8a37264576eba6722afa2dabe585bee0248a8c434`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 13.7 MB (13681970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ae0207198a3255726cc8557821cfde799fae904dd24a9c36ccee160e7d2989`  
		Last Modified: Mon, 23 Mar 2026 21:32:57 GMT  
		Size: 153.7 MB (153673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d4c9cd4325f2571654f24b325523ef79773d87fb951673c703cfabf3f43aa5`  
		Last Modified: Mon, 23 Mar 2026 21:32:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:ab342386cefb634491e1d5f2506ae9fc03b9c751966a043d5f64c11f0649020a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e573160abafe3de68a1a7e2e1cc47fe0c34936749ecbca49d88a198e4431ebf`

```dockerfile
```

-	Layers:
	-	`sha256:fd8de3eb23b5baac30eec58502a79e393804c6facd7fa1c570ff4a1b63bfdeac`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 3.5 MB (3516840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea448e68e834543f49ce7ae9f41c3656ba6443a98ff48cfd359eadcb2e222fd`  
		Last Modified: Mon, 23 Mar 2026 21:32:53 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:f549dfa0f470bccc18f44ca1a2f507ecafeec4553ab93d465a8d15479a3be0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238420685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8640b018bfaaec34fa1df815b396cf927c2a82a76f28a4d17144abf7fe834b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:35 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:35 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064521911821dc19024bfe059748914160b230bbe68557dd98762deb1b6b43b6`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 891.3 KB (891302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1567db9f8b8a62a578279fda7f78fd3faccaf1d3269de769cafa7d141f80c97`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff613941cfbd284f01e4a2ba730151924641d94d1d7ea7d28a647526d47997b`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 13.7 MB (13682926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2598f4dbb9b4dbcefda013229846cea551c0c45feae80f8ec7ff020211922e`  
		Last Modified: Mon, 23 Mar 2026 21:33:24 GMT  
		Size: 164.8 MB (164807296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b879ea0c6b80ed51f2886e5ca6537a10ba26fbfd50daf9872ccb37d9bef6b0`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:5fbb4a54c0909702a7bbca920d61aa85ae8d4e32876f1e08a1a9c72edbb1f002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ef8a87c4cb31dbacba647a84c613cebfe2b32ffb09339785b694ca7a7b18fa`

```dockerfile
```

-	Layers:
	-	`sha256:2546e7cffbbfdc7c439fa4fb5505c6184fec8500270676ce9f94c6a4da52fe54`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 3.5 MB (3516346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9c9c17adf902326fb0ef26ddad508ee7c1baa23d3dc8d0cf980e7f58b71b52`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-bookworm`

```console
$ docker pull ghost@sha256:1582ff7d419839eea2d5d75867703a6344f0df818f1b31680fe68b2c77940ea7
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
$ docker pull ghost@sha256:2f9bb6d9eb2bfab9f2dfd77fdd9a821189a3b6d68f1317070ecbc3afb227e4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248679987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e570be6b9273a46c7912f31b3ae1719a8b895f687517bf63e96c538828f85387`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:26 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:56 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:56 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:56 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:56 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a57a621e2f90878c454c2900fb34b2e03bedcc306a9222c107772613672dfc9`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 1.2 MB (1247569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaa7fbb100f45ffee6750ca12ac096340c2913a360a8beeda5ba4b01d694e28`  
		Last Modified: Mon, 23 Mar 2026 21:33:38 GMT  
		Size: 13.7 MB (13681613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daadcb48818fecaf7145d281b62f72d64c73203df1b5c1cba03554f9ef67687`  
		Last Modified: Mon, 23 Mar 2026 21:33:41 GMT  
		Size: 153.8 MB (153847869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df50c7aa534128b8fa46cf0add79d4ffb8b57bbc4af16455f1339cd50731dda`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:0ea1489cab0174441d8a6e634f79e701d7a3e677c0919a594d84fc440955add4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e628c3c13542d24af4a7d4661639ed0a14f390a888b038f268dfdcf98e81fc2`

```dockerfile
```

-	Layers:
	-	`sha256:192a7f22b112d9ec1b7ef28fb42ad6fcbdd2f4687d1eaee3e28d6aa445a210f3`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 5.7 MB (5728841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d568062998c575776388d04c7090d619bb718a28c6d2f0001b4ec6e6d8a6bd`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:20fdc88d1557e233521af22d56acb959c23fb93c1687ca379d2de2979762415c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239965609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05013a90d878f774ed0f6cad6150f890362b5132d3dd76a36d2937df4b65ec87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:23 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:33:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:33:45 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:33:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:33:45 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:33:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9d4a88a3446ee882364a12dd45715592c8caf3941e70428d8bf80a50dc475`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 1.2 MB (1214351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66730a7e2a8e64649282d3e679b71b0794a963394be7f23532455764aaa4fac3`  
		Last Modified: Mon, 23 Mar 2026 21:34:30 GMT  
		Size: 13.7 MB (13671566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d599dc93bd69676edfb560878bfe6d869ac45745b0979d94d2aa4fb664600704`  
		Last Modified: Mon, 23 Mar 2026 21:34:33 GMT  
		Size: 154.7 MB (154747466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692414abc743d668b09fde51ab99e741deb58e289ed9f52ecfb271b5129869a`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:37f22098bff7f063d035344e295141ddd850fbedaf5a82fb1c7f24a0d448cc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5758123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8956d6025e4be66b9993790b8db707e33f9118b5022cde428d8bd8c35b1941`

```dockerfile
```

-	Layers:
	-	`sha256:09a626197c2b8838253dd647d94b0318b368f11d81cda127086788e043553976`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 5.7 MB (5731638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02b21ea1347601077dbf5d111f5fe8fd9ddeb4bf593027117a925952bfcae826`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:532df5ac9173a7ebb5a9890200818ebb00a4cd93c0d45ed5dbb11b8f7128f8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248989503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083043a4af7a3b001169fa4eb222731b19ebdbbafc21e6003b22609973e60670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:55 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:55 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8884c3f01372d2e4a7474c46a6a3f4c832daab7aa1b99822ebb911326b6420ce`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 1.2 MB (1201503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea814e0687d3f76992f290145881ac774ea1dda23513db4a31b5aaf6921c4d6`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 13.7 MB (13683347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f8618f0b7718f83c70cf3af35e1bf838e322049b898af2e5f6a6b1ae38a27e`  
		Last Modified: Mon, 23 Mar 2026 21:33:44 GMT  
		Size: 154.2 MB (154187137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b24587a07d6009c6736c1b37ccd2617dd2215278bea85ea10c28dd7ceb4d9f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:c2bddbf5e655a85a72932c684c632cbe432aa824337d46b3d5c5fbf32be2cf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77145a0f19a1617977a8e7073d6dc1b0643b9b715a13d4400fff20c584ace01`

```dockerfile
```

-	Layers:
	-	`sha256:ebfad0586565c6db9343b78119476e7c9e5d0c3abfc1eb96c805c1962b5346d4`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 5.7 MB (5729192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b6450155958226ae3645f5b860b28cf158b635f3e0218e7046a3ddacdb8be3f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:10c95b76ee1638c2b14965868938bf3df60c5420a9c51005d92d61eaf5eec7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250552024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd62e5e5b20c5c893d64d2a0d63d8909b9c128398afc662a97ef4caab16ea690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 21:02:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 21:02:36 GMT
ENV NODE_ENV=production
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:06 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:06 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb0991be587623bd7e5d5529f267aa799aa553646701411b326cf0bedc49f08`  
		Last Modified: Fri, 20 Mar 2026 21:12:35 GMT  
		Size: 1.2 MB (1221347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb6fab34355db319427c08ce5355f0ce4a7847585df335e90fcb1501e579317`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 13.7 MB (13685080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98733d2270747b6d6976cba73d3d17322fefe55018112ba288b4617d60a4cf07`  
		Last Modified: Mon, 23 Mar 2026 21:33:09 GMT  
		Size: 156.9 MB (156906054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913dbdccceed1570268555c5dc113a437a4913eff641d7dd82c7b1f6f15976f`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:a55cf19c79761f21d1352e52d9edb2dda75bd55e2742b5dfd85703eb0502f18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1796ca6388170fe21901544915383a04e469322a542570b61fb8ea477b7d85`

```dockerfile
```

-	Layers:
	-	`sha256:97cd11b0670fff5b1f270a8d33607a18e76d5a242238ee55b75cc6ecaa9ba413`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 5.7 MB (5722666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2b1cc7ccf96fcd3b69663a88f6246e4d6fb638b7d3695a1909fd6180eeb831`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22`

```console
$ docker pull ghost@sha256:1582ff7d419839eea2d5d75867703a6344f0df818f1b31680fe68b2c77940ea7
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

### `ghost:6.22` - linux; amd64

```console
$ docker pull ghost@sha256:2f9bb6d9eb2bfab9f2dfd77fdd9a821189a3b6d68f1317070ecbc3afb227e4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248679987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e570be6b9273a46c7912f31b3ae1719a8b895f687517bf63e96c538828f85387`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:26 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:56 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:56 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:56 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:56 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a57a621e2f90878c454c2900fb34b2e03bedcc306a9222c107772613672dfc9`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 1.2 MB (1247569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaa7fbb100f45ffee6750ca12ac096340c2913a360a8beeda5ba4b01d694e28`  
		Last Modified: Mon, 23 Mar 2026 21:33:38 GMT  
		Size: 13.7 MB (13681613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daadcb48818fecaf7145d281b62f72d64c73203df1b5c1cba03554f9ef67687`  
		Last Modified: Mon, 23 Mar 2026 21:33:41 GMT  
		Size: 153.8 MB (153847869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df50c7aa534128b8fa46cf0add79d4ffb8b57bbc4af16455f1339cd50731dda`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22` - unknown; unknown

```console
$ docker pull ghost@sha256:0ea1489cab0174441d8a6e634f79e701d7a3e677c0919a594d84fc440955add4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e628c3c13542d24af4a7d4661639ed0a14f390a888b038f268dfdcf98e81fc2`

```dockerfile
```

-	Layers:
	-	`sha256:192a7f22b112d9ec1b7ef28fb42ad6fcbdd2f4687d1eaee3e28d6aa445a210f3`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 5.7 MB (5728841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d568062998c575776388d04c7090d619bb718a28c6d2f0001b4ec6e6d8a6bd`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22` - linux; arm variant v7

```console
$ docker pull ghost@sha256:20fdc88d1557e233521af22d56acb959c23fb93c1687ca379d2de2979762415c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239965609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05013a90d878f774ed0f6cad6150f890362b5132d3dd76a36d2937df4b65ec87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:23 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:33:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:33:45 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:33:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:33:45 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:33:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9d4a88a3446ee882364a12dd45715592c8caf3941e70428d8bf80a50dc475`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 1.2 MB (1214351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66730a7e2a8e64649282d3e679b71b0794a963394be7f23532455764aaa4fac3`  
		Last Modified: Mon, 23 Mar 2026 21:34:30 GMT  
		Size: 13.7 MB (13671566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d599dc93bd69676edfb560878bfe6d869ac45745b0979d94d2aa4fb664600704`  
		Last Modified: Mon, 23 Mar 2026 21:34:33 GMT  
		Size: 154.7 MB (154747466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692414abc743d668b09fde51ab99e741deb58e289ed9f52ecfb271b5129869a`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22` - unknown; unknown

```console
$ docker pull ghost@sha256:37f22098bff7f063d035344e295141ddd850fbedaf5a82fb1c7f24a0d448cc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5758123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8956d6025e4be66b9993790b8db707e33f9118b5022cde428d8bd8c35b1941`

```dockerfile
```

-	Layers:
	-	`sha256:09a626197c2b8838253dd647d94b0318b368f11d81cda127086788e043553976`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 5.7 MB (5731638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02b21ea1347601077dbf5d111f5fe8fd9ddeb4bf593027117a925952bfcae826`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:532df5ac9173a7ebb5a9890200818ebb00a4cd93c0d45ed5dbb11b8f7128f8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248989503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083043a4af7a3b001169fa4eb222731b19ebdbbafc21e6003b22609973e60670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:55 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:55 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8884c3f01372d2e4a7474c46a6a3f4c832daab7aa1b99822ebb911326b6420ce`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 1.2 MB (1201503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea814e0687d3f76992f290145881ac774ea1dda23513db4a31b5aaf6921c4d6`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 13.7 MB (13683347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f8618f0b7718f83c70cf3af35e1bf838e322049b898af2e5f6a6b1ae38a27e`  
		Last Modified: Mon, 23 Mar 2026 21:33:44 GMT  
		Size: 154.2 MB (154187137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b24587a07d6009c6736c1b37ccd2617dd2215278bea85ea10c28dd7ceb4d9f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22` - unknown; unknown

```console
$ docker pull ghost@sha256:c2bddbf5e655a85a72932c684c632cbe432aa824337d46b3d5c5fbf32be2cf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77145a0f19a1617977a8e7073d6dc1b0643b9b715a13d4400fff20c584ace01`

```dockerfile
```

-	Layers:
	-	`sha256:ebfad0586565c6db9343b78119476e7c9e5d0c3abfc1eb96c805c1962b5346d4`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 5.7 MB (5729192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b6450155958226ae3645f5b860b28cf158b635f3e0218e7046a3ddacdb8be3f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22` - linux; s390x

```console
$ docker pull ghost@sha256:10c95b76ee1638c2b14965868938bf3df60c5420a9c51005d92d61eaf5eec7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250552024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd62e5e5b20c5c893d64d2a0d63d8909b9c128398afc662a97ef4caab16ea690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 21:02:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 21:02:36 GMT
ENV NODE_ENV=production
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:06 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:06 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb0991be587623bd7e5d5529f267aa799aa553646701411b326cf0bedc49f08`  
		Last Modified: Fri, 20 Mar 2026 21:12:35 GMT  
		Size: 1.2 MB (1221347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb6fab34355db319427c08ce5355f0ce4a7847585df335e90fcb1501e579317`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 13.7 MB (13685080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98733d2270747b6d6976cba73d3d17322fefe55018112ba288b4617d60a4cf07`  
		Last Modified: Mon, 23 Mar 2026 21:33:09 GMT  
		Size: 156.9 MB (156906054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913dbdccceed1570268555c5dc113a437a4913eff641d7dd82c7b1f6f15976f`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22` - unknown; unknown

```console
$ docker pull ghost@sha256:a55cf19c79761f21d1352e52d9edb2dda75bd55e2742b5dfd85703eb0502f18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1796ca6388170fe21901544915383a04e469322a542570b61fb8ea477b7d85`

```dockerfile
```

-	Layers:
	-	`sha256:97cd11b0670fff5b1f270a8d33607a18e76d5a242238ee55b75cc6ecaa9ba413`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 5.7 MB (5722666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2b1cc7ccf96fcd3b69663a88f6246e4d6fb638b7d3695a1909fd6180eeb831`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22-alpine`

```console
$ docker pull ghost@sha256:4f02907212c3a27dac837a51ace205f13d697c8e5d7ce611cbfb0e4d29551142
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.22-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:323e7dc6f9c45075623fbc7b0ab34cb4ed4833b6f4e3a4a654cb68cfc9bdc21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226302331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a12d8a5f0844d7eebaf1a0193281509a2cc5e793babb6f0ac8211a3677e90e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:51 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:15 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:15 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d61e4e317c93f7baa694fdee1e67ab024f703469c8f8e8c9260fe7967a5db`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8c827691e7d79dde0d5895995f8d82a90e4f56d368553bb000e1b8dda8c474`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 928.3 KB (928324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a0a060db6076d19c841d8a37264576eba6722afa2dabe585bee0248a8c434`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 13.7 MB (13681970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ae0207198a3255726cc8557821cfde799fae904dd24a9c36ccee160e7d2989`  
		Last Modified: Mon, 23 Mar 2026 21:32:57 GMT  
		Size: 153.7 MB (153673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d4c9cd4325f2571654f24b325523ef79773d87fb951673c703cfabf3f43aa5`  
		Last Modified: Mon, 23 Mar 2026 21:32:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:ab342386cefb634491e1d5f2506ae9fc03b9c751966a043d5f64c11f0649020a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e573160abafe3de68a1a7e2e1cc47fe0c34936749ecbca49d88a198e4431ebf`

```dockerfile
```

-	Layers:
	-	`sha256:fd8de3eb23b5baac30eec58502a79e393804c6facd7fa1c570ff4a1b63bfdeac`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 3.5 MB (3516840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea448e68e834543f49ce7ae9f41c3656ba6443a98ff48cfd359eadcb2e222fd`  
		Last Modified: Mon, 23 Mar 2026 21:32:53 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:f549dfa0f470bccc18f44ca1a2f507ecafeec4553ab93d465a8d15479a3be0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238420685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8640b018bfaaec34fa1df815b396cf927c2a82a76f28a4d17144abf7fe834b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:35 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:35 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064521911821dc19024bfe059748914160b230bbe68557dd98762deb1b6b43b6`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 891.3 KB (891302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1567db9f8b8a62a578279fda7f78fd3faccaf1d3269de769cafa7d141f80c97`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff613941cfbd284f01e4a2ba730151924641d94d1d7ea7d28a647526d47997b`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 13.7 MB (13682926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2598f4dbb9b4dbcefda013229846cea551c0c45feae80f8ec7ff020211922e`  
		Last Modified: Mon, 23 Mar 2026 21:33:24 GMT  
		Size: 164.8 MB (164807296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b879ea0c6b80ed51f2886e5ca6537a10ba26fbfd50daf9872ccb37d9bef6b0`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:5fbb4a54c0909702a7bbca920d61aa85ae8d4e32876f1e08a1a9c72edbb1f002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ef8a87c4cb31dbacba647a84c613cebfe2b32ffb09339785b694ca7a7b18fa`

```dockerfile
```

-	Layers:
	-	`sha256:2546e7cffbbfdc7c439fa4fb5505c6184fec8500270676ce9f94c6a4da52fe54`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 3.5 MB (3516346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9c9c17adf902326fb0ef26ddad508ee7c1baa23d3dc8d0cf980e7f58b71b52`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22-alpine3.23`

```console
$ docker pull ghost@sha256:4f02907212c3a27dac837a51ace205f13d697c8e5d7ce611cbfb0e4d29551142
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.22-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:323e7dc6f9c45075623fbc7b0ab34cb4ed4833b6f4e3a4a654cb68cfc9bdc21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226302331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a12d8a5f0844d7eebaf1a0193281509a2cc5e793babb6f0ac8211a3677e90e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:51 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:15 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:15 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d61e4e317c93f7baa694fdee1e67ab024f703469c8f8e8c9260fe7967a5db`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8c827691e7d79dde0d5895995f8d82a90e4f56d368553bb000e1b8dda8c474`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 928.3 KB (928324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a0a060db6076d19c841d8a37264576eba6722afa2dabe585bee0248a8c434`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 13.7 MB (13681970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ae0207198a3255726cc8557821cfde799fae904dd24a9c36ccee160e7d2989`  
		Last Modified: Mon, 23 Mar 2026 21:32:57 GMT  
		Size: 153.7 MB (153673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d4c9cd4325f2571654f24b325523ef79773d87fb951673c703cfabf3f43aa5`  
		Last Modified: Mon, 23 Mar 2026 21:32:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:ab342386cefb634491e1d5f2506ae9fc03b9c751966a043d5f64c11f0649020a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e573160abafe3de68a1a7e2e1cc47fe0c34936749ecbca49d88a198e4431ebf`

```dockerfile
```

-	Layers:
	-	`sha256:fd8de3eb23b5baac30eec58502a79e393804c6facd7fa1c570ff4a1b63bfdeac`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 3.5 MB (3516840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea448e68e834543f49ce7ae9f41c3656ba6443a98ff48cfd359eadcb2e222fd`  
		Last Modified: Mon, 23 Mar 2026 21:32:53 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:f549dfa0f470bccc18f44ca1a2f507ecafeec4553ab93d465a8d15479a3be0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238420685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8640b018bfaaec34fa1df815b396cf927c2a82a76f28a4d17144abf7fe834b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:35 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:35 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064521911821dc19024bfe059748914160b230bbe68557dd98762deb1b6b43b6`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 891.3 KB (891302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1567db9f8b8a62a578279fda7f78fd3faccaf1d3269de769cafa7d141f80c97`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff613941cfbd284f01e4a2ba730151924641d94d1d7ea7d28a647526d47997b`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 13.7 MB (13682926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2598f4dbb9b4dbcefda013229846cea551c0c45feae80f8ec7ff020211922e`  
		Last Modified: Mon, 23 Mar 2026 21:33:24 GMT  
		Size: 164.8 MB (164807296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b879ea0c6b80ed51f2886e5ca6537a10ba26fbfd50daf9872ccb37d9bef6b0`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:5fbb4a54c0909702a7bbca920d61aa85ae8d4e32876f1e08a1a9c72edbb1f002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ef8a87c4cb31dbacba647a84c613cebfe2b32ffb09339785b694ca7a7b18fa`

```dockerfile
```

-	Layers:
	-	`sha256:2546e7cffbbfdc7c439fa4fb5505c6184fec8500270676ce9f94c6a4da52fe54`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 3.5 MB (3516346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9c9c17adf902326fb0ef26ddad508ee7c1baa23d3dc8d0cf980e7f58b71b52`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22-bookworm`

```console
$ docker pull ghost@sha256:1582ff7d419839eea2d5d75867703a6344f0df818f1b31680fe68b2c77940ea7
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

### `ghost:6.22-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:2f9bb6d9eb2bfab9f2dfd77fdd9a821189a3b6d68f1317070ecbc3afb227e4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248679987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e570be6b9273a46c7912f31b3ae1719a8b895f687517bf63e96c538828f85387`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:26 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:56 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:56 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:56 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:56 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a57a621e2f90878c454c2900fb34b2e03bedcc306a9222c107772613672dfc9`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 1.2 MB (1247569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaa7fbb100f45ffee6750ca12ac096340c2913a360a8beeda5ba4b01d694e28`  
		Last Modified: Mon, 23 Mar 2026 21:33:38 GMT  
		Size: 13.7 MB (13681613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daadcb48818fecaf7145d281b62f72d64c73203df1b5c1cba03554f9ef67687`  
		Last Modified: Mon, 23 Mar 2026 21:33:41 GMT  
		Size: 153.8 MB (153847869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df50c7aa534128b8fa46cf0add79d4ffb8b57bbc4af16455f1339cd50731dda`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:0ea1489cab0174441d8a6e634f79e701d7a3e677c0919a594d84fc440955add4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e628c3c13542d24af4a7d4661639ed0a14f390a888b038f268dfdcf98e81fc2`

```dockerfile
```

-	Layers:
	-	`sha256:192a7f22b112d9ec1b7ef28fb42ad6fcbdd2f4687d1eaee3e28d6aa445a210f3`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 5.7 MB (5728841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d568062998c575776388d04c7090d619bb718a28c6d2f0001b4ec6e6d8a6bd`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:20fdc88d1557e233521af22d56acb959c23fb93c1687ca379d2de2979762415c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239965609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05013a90d878f774ed0f6cad6150f890362b5132d3dd76a36d2937df4b65ec87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:23 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:33:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:33:45 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:33:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:33:45 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:33:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9d4a88a3446ee882364a12dd45715592c8caf3941e70428d8bf80a50dc475`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 1.2 MB (1214351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66730a7e2a8e64649282d3e679b71b0794a963394be7f23532455764aaa4fac3`  
		Last Modified: Mon, 23 Mar 2026 21:34:30 GMT  
		Size: 13.7 MB (13671566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d599dc93bd69676edfb560878bfe6d869ac45745b0979d94d2aa4fb664600704`  
		Last Modified: Mon, 23 Mar 2026 21:34:33 GMT  
		Size: 154.7 MB (154747466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692414abc743d668b09fde51ab99e741deb58e289ed9f52ecfb271b5129869a`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:37f22098bff7f063d035344e295141ddd850fbedaf5a82fb1c7f24a0d448cc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5758123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8956d6025e4be66b9993790b8db707e33f9118b5022cde428d8bd8c35b1941`

```dockerfile
```

-	Layers:
	-	`sha256:09a626197c2b8838253dd647d94b0318b368f11d81cda127086788e043553976`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 5.7 MB (5731638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02b21ea1347601077dbf5d111f5fe8fd9ddeb4bf593027117a925952bfcae826`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:532df5ac9173a7ebb5a9890200818ebb00a4cd93c0d45ed5dbb11b8f7128f8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248989503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083043a4af7a3b001169fa4eb222731b19ebdbbafc21e6003b22609973e60670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:55 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:55 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8884c3f01372d2e4a7474c46a6a3f4c832daab7aa1b99822ebb911326b6420ce`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 1.2 MB (1201503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea814e0687d3f76992f290145881ac774ea1dda23513db4a31b5aaf6921c4d6`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 13.7 MB (13683347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f8618f0b7718f83c70cf3af35e1bf838e322049b898af2e5f6a6b1ae38a27e`  
		Last Modified: Mon, 23 Mar 2026 21:33:44 GMT  
		Size: 154.2 MB (154187137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b24587a07d6009c6736c1b37ccd2617dd2215278bea85ea10c28dd7ceb4d9f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:c2bddbf5e655a85a72932c684c632cbe432aa824337d46b3d5c5fbf32be2cf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77145a0f19a1617977a8e7073d6dc1b0643b9b715a13d4400fff20c584ace01`

```dockerfile
```

-	Layers:
	-	`sha256:ebfad0586565c6db9343b78119476e7c9e5d0c3abfc1eb96c805c1962b5346d4`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 5.7 MB (5729192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b6450155958226ae3645f5b860b28cf158b635f3e0218e7046a3ddacdb8be3f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:10c95b76ee1638c2b14965868938bf3df60c5420a9c51005d92d61eaf5eec7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250552024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd62e5e5b20c5c893d64d2a0d63d8909b9c128398afc662a97ef4caab16ea690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 21:02:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 21:02:36 GMT
ENV NODE_ENV=production
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:06 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:06 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb0991be587623bd7e5d5529f267aa799aa553646701411b326cf0bedc49f08`  
		Last Modified: Fri, 20 Mar 2026 21:12:35 GMT  
		Size: 1.2 MB (1221347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb6fab34355db319427c08ce5355f0ce4a7847585df335e90fcb1501e579317`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 13.7 MB (13685080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98733d2270747b6d6976cba73d3d17322fefe55018112ba288b4617d60a4cf07`  
		Last Modified: Mon, 23 Mar 2026 21:33:09 GMT  
		Size: 156.9 MB (156906054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913dbdccceed1570268555c5dc113a437a4913eff641d7dd82c7b1f6f15976f`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:a55cf19c79761f21d1352e52d9edb2dda75bd55e2742b5dfd85703eb0502f18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1796ca6388170fe21901544915383a04e469322a542570b61fb8ea477b7d85`

```dockerfile
```

-	Layers:
	-	`sha256:97cd11b0670fff5b1f270a8d33607a18e76d5a242238ee55b75cc6ecaa9ba413`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 5.7 MB (5722666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2b1cc7ccf96fcd3b69663a88f6246e4d6fb638b7d3695a1909fd6180eeb831`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22.1`

```console
$ docker pull ghost@sha256:1582ff7d419839eea2d5d75867703a6344f0df818f1b31680fe68b2c77940ea7
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

### `ghost:6.22.1` - linux; amd64

```console
$ docker pull ghost@sha256:2f9bb6d9eb2bfab9f2dfd77fdd9a821189a3b6d68f1317070ecbc3afb227e4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248679987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e570be6b9273a46c7912f31b3ae1719a8b895f687517bf63e96c538828f85387`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:26 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:56 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:56 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:56 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:56 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a57a621e2f90878c454c2900fb34b2e03bedcc306a9222c107772613672dfc9`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 1.2 MB (1247569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaa7fbb100f45ffee6750ca12ac096340c2913a360a8beeda5ba4b01d694e28`  
		Last Modified: Mon, 23 Mar 2026 21:33:38 GMT  
		Size: 13.7 MB (13681613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daadcb48818fecaf7145d281b62f72d64c73203df1b5c1cba03554f9ef67687`  
		Last Modified: Mon, 23 Mar 2026 21:33:41 GMT  
		Size: 153.8 MB (153847869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df50c7aa534128b8fa46cf0add79d4ffb8b57bbc4af16455f1339cd50731dda`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.1` - unknown; unknown

```console
$ docker pull ghost@sha256:0ea1489cab0174441d8a6e634f79e701d7a3e677c0919a594d84fc440955add4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e628c3c13542d24af4a7d4661639ed0a14f390a888b038f268dfdcf98e81fc2`

```dockerfile
```

-	Layers:
	-	`sha256:192a7f22b112d9ec1b7ef28fb42ad6fcbdd2f4687d1eaee3e28d6aa445a210f3`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 5.7 MB (5728841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d568062998c575776388d04c7090d619bb718a28c6d2f0001b4ec6e6d8a6bd`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.1` - linux; arm variant v7

```console
$ docker pull ghost@sha256:20fdc88d1557e233521af22d56acb959c23fb93c1687ca379d2de2979762415c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239965609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05013a90d878f774ed0f6cad6150f890362b5132d3dd76a36d2937df4b65ec87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:23 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:33:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:33:45 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:33:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:33:45 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:33:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9d4a88a3446ee882364a12dd45715592c8caf3941e70428d8bf80a50dc475`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 1.2 MB (1214351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66730a7e2a8e64649282d3e679b71b0794a963394be7f23532455764aaa4fac3`  
		Last Modified: Mon, 23 Mar 2026 21:34:30 GMT  
		Size: 13.7 MB (13671566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d599dc93bd69676edfb560878bfe6d869ac45745b0979d94d2aa4fb664600704`  
		Last Modified: Mon, 23 Mar 2026 21:34:33 GMT  
		Size: 154.7 MB (154747466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692414abc743d668b09fde51ab99e741deb58e289ed9f52ecfb271b5129869a`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.1` - unknown; unknown

```console
$ docker pull ghost@sha256:37f22098bff7f063d035344e295141ddd850fbedaf5a82fb1c7f24a0d448cc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5758123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8956d6025e4be66b9993790b8db707e33f9118b5022cde428d8bd8c35b1941`

```dockerfile
```

-	Layers:
	-	`sha256:09a626197c2b8838253dd647d94b0318b368f11d81cda127086788e043553976`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 5.7 MB (5731638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02b21ea1347601077dbf5d111f5fe8fd9ddeb4bf593027117a925952bfcae826`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.1` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:532df5ac9173a7ebb5a9890200818ebb00a4cd93c0d45ed5dbb11b8f7128f8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248989503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083043a4af7a3b001169fa4eb222731b19ebdbbafc21e6003b22609973e60670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:55 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:55 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8884c3f01372d2e4a7474c46a6a3f4c832daab7aa1b99822ebb911326b6420ce`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 1.2 MB (1201503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea814e0687d3f76992f290145881ac774ea1dda23513db4a31b5aaf6921c4d6`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 13.7 MB (13683347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f8618f0b7718f83c70cf3af35e1bf838e322049b898af2e5f6a6b1ae38a27e`  
		Last Modified: Mon, 23 Mar 2026 21:33:44 GMT  
		Size: 154.2 MB (154187137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b24587a07d6009c6736c1b37ccd2617dd2215278bea85ea10c28dd7ceb4d9f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.1` - unknown; unknown

```console
$ docker pull ghost@sha256:c2bddbf5e655a85a72932c684c632cbe432aa824337d46b3d5c5fbf32be2cf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77145a0f19a1617977a8e7073d6dc1b0643b9b715a13d4400fff20c584ace01`

```dockerfile
```

-	Layers:
	-	`sha256:ebfad0586565c6db9343b78119476e7c9e5d0c3abfc1eb96c805c1962b5346d4`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 5.7 MB (5729192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b6450155958226ae3645f5b860b28cf158b635f3e0218e7046a3ddacdb8be3f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.1` - linux; s390x

```console
$ docker pull ghost@sha256:10c95b76ee1638c2b14965868938bf3df60c5420a9c51005d92d61eaf5eec7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250552024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd62e5e5b20c5c893d64d2a0d63d8909b9c128398afc662a97ef4caab16ea690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 21:02:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 21:02:36 GMT
ENV NODE_ENV=production
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:06 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:06 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb0991be587623bd7e5d5529f267aa799aa553646701411b326cf0bedc49f08`  
		Last Modified: Fri, 20 Mar 2026 21:12:35 GMT  
		Size: 1.2 MB (1221347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb6fab34355db319427c08ce5355f0ce4a7847585df335e90fcb1501e579317`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 13.7 MB (13685080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98733d2270747b6d6976cba73d3d17322fefe55018112ba288b4617d60a4cf07`  
		Last Modified: Mon, 23 Mar 2026 21:33:09 GMT  
		Size: 156.9 MB (156906054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913dbdccceed1570268555c5dc113a437a4913eff641d7dd82c7b1f6f15976f`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.1` - unknown; unknown

```console
$ docker pull ghost@sha256:a55cf19c79761f21d1352e52d9edb2dda75bd55e2742b5dfd85703eb0502f18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1796ca6388170fe21901544915383a04e469322a542570b61fb8ea477b7d85`

```dockerfile
```

-	Layers:
	-	`sha256:97cd11b0670fff5b1f270a8d33607a18e76d5a242238ee55b75cc6ecaa9ba413`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 5.7 MB (5722666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2b1cc7ccf96fcd3b69663a88f6246e4d6fb638b7d3695a1909fd6180eeb831`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22.1-alpine`

```console
$ docker pull ghost@sha256:4f02907212c3a27dac837a51ace205f13d697c8e5d7ce611cbfb0e4d29551142
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.22.1-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:323e7dc6f9c45075623fbc7b0ab34cb4ed4833b6f4e3a4a654cb68cfc9bdc21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226302331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a12d8a5f0844d7eebaf1a0193281509a2cc5e793babb6f0ac8211a3677e90e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:51 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:15 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:15 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d61e4e317c93f7baa694fdee1e67ab024f703469c8f8e8c9260fe7967a5db`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8c827691e7d79dde0d5895995f8d82a90e4f56d368553bb000e1b8dda8c474`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 928.3 KB (928324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a0a060db6076d19c841d8a37264576eba6722afa2dabe585bee0248a8c434`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 13.7 MB (13681970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ae0207198a3255726cc8557821cfde799fae904dd24a9c36ccee160e7d2989`  
		Last Modified: Mon, 23 Mar 2026 21:32:57 GMT  
		Size: 153.7 MB (153673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d4c9cd4325f2571654f24b325523ef79773d87fb951673c703cfabf3f43aa5`  
		Last Modified: Mon, 23 Mar 2026 21:32:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.1-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:ab342386cefb634491e1d5f2506ae9fc03b9c751966a043d5f64c11f0649020a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e573160abafe3de68a1a7e2e1cc47fe0c34936749ecbca49d88a198e4431ebf`

```dockerfile
```

-	Layers:
	-	`sha256:fd8de3eb23b5baac30eec58502a79e393804c6facd7fa1c570ff4a1b63bfdeac`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 3.5 MB (3516840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea448e68e834543f49ce7ae9f41c3656ba6443a98ff48cfd359eadcb2e222fd`  
		Last Modified: Mon, 23 Mar 2026 21:32:53 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.1-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:f549dfa0f470bccc18f44ca1a2f507ecafeec4553ab93d465a8d15479a3be0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238420685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8640b018bfaaec34fa1df815b396cf927c2a82a76f28a4d17144abf7fe834b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:35 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:35 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064521911821dc19024bfe059748914160b230bbe68557dd98762deb1b6b43b6`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 891.3 KB (891302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1567db9f8b8a62a578279fda7f78fd3faccaf1d3269de769cafa7d141f80c97`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff613941cfbd284f01e4a2ba730151924641d94d1d7ea7d28a647526d47997b`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 13.7 MB (13682926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2598f4dbb9b4dbcefda013229846cea551c0c45feae80f8ec7ff020211922e`  
		Last Modified: Mon, 23 Mar 2026 21:33:24 GMT  
		Size: 164.8 MB (164807296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b879ea0c6b80ed51f2886e5ca6537a10ba26fbfd50daf9872ccb37d9bef6b0`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.1-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:5fbb4a54c0909702a7bbca920d61aa85ae8d4e32876f1e08a1a9c72edbb1f002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ef8a87c4cb31dbacba647a84c613cebfe2b32ffb09339785b694ca7a7b18fa`

```dockerfile
```

-	Layers:
	-	`sha256:2546e7cffbbfdc7c439fa4fb5505c6184fec8500270676ce9f94c6a4da52fe54`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 3.5 MB (3516346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9c9c17adf902326fb0ef26ddad508ee7c1baa23d3dc8d0cf980e7f58b71b52`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22.1-alpine3.23`

```console
$ docker pull ghost@sha256:4f02907212c3a27dac837a51ace205f13d697c8e5d7ce611cbfb0e4d29551142
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.22.1-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:323e7dc6f9c45075623fbc7b0ab34cb4ed4833b6f4e3a4a654cb68cfc9bdc21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226302331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a12d8a5f0844d7eebaf1a0193281509a2cc5e793babb6f0ac8211a3677e90e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:51 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:15 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:15 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d61e4e317c93f7baa694fdee1e67ab024f703469c8f8e8c9260fe7967a5db`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8c827691e7d79dde0d5895995f8d82a90e4f56d368553bb000e1b8dda8c474`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 928.3 KB (928324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a0a060db6076d19c841d8a37264576eba6722afa2dabe585bee0248a8c434`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 13.7 MB (13681970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ae0207198a3255726cc8557821cfde799fae904dd24a9c36ccee160e7d2989`  
		Last Modified: Mon, 23 Mar 2026 21:32:57 GMT  
		Size: 153.7 MB (153673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d4c9cd4325f2571654f24b325523ef79773d87fb951673c703cfabf3f43aa5`  
		Last Modified: Mon, 23 Mar 2026 21:32:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.1-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:ab342386cefb634491e1d5f2506ae9fc03b9c751966a043d5f64c11f0649020a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e573160abafe3de68a1a7e2e1cc47fe0c34936749ecbca49d88a198e4431ebf`

```dockerfile
```

-	Layers:
	-	`sha256:fd8de3eb23b5baac30eec58502a79e393804c6facd7fa1c570ff4a1b63bfdeac`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 3.5 MB (3516840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea448e68e834543f49ce7ae9f41c3656ba6443a98ff48cfd359eadcb2e222fd`  
		Last Modified: Mon, 23 Mar 2026 21:32:53 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:f549dfa0f470bccc18f44ca1a2f507ecafeec4553ab93d465a8d15479a3be0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238420685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8640b018bfaaec34fa1df815b396cf927c2a82a76f28a4d17144abf7fe834b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:35 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:35 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064521911821dc19024bfe059748914160b230bbe68557dd98762deb1b6b43b6`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 891.3 KB (891302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1567db9f8b8a62a578279fda7f78fd3faccaf1d3269de769cafa7d141f80c97`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff613941cfbd284f01e4a2ba730151924641d94d1d7ea7d28a647526d47997b`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 13.7 MB (13682926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2598f4dbb9b4dbcefda013229846cea551c0c45feae80f8ec7ff020211922e`  
		Last Modified: Mon, 23 Mar 2026 21:33:24 GMT  
		Size: 164.8 MB (164807296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b879ea0c6b80ed51f2886e5ca6537a10ba26fbfd50daf9872ccb37d9bef6b0`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.1-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:5fbb4a54c0909702a7bbca920d61aa85ae8d4e32876f1e08a1a9c72edbb1f002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ef8a87c4cb31dbacba647a84c613cebfe2b32ffb09339785b694ca7a7b18fa`

```dockerfile
```

-	Layers:
	-	`sha256:2546e7cffbbfdc7c439fa4fb5505c6184fec8500270676ce9f94c6a4da52fe54`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 3.5 MB (3516346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9c9c17adf902326fb0ef26ddad508ee7c1baa23d3dc8d0cf980e7f58b71b52`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.22.1-bookworm`

```console
$ docker pull ghost@sha256:1582ff7d419839eea2d5d75867703a6344f0df818f1b31680fe68b2c77940ea7
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

### `ghost:6.22.1-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:2f9bb6d9eb2bfab9f2dfd77fdd9a821189a3b6d68f1317070ecbc3afb227e4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248679987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e570be6b9273a46c7912f31b3ae1719a8b895f687517bf63e96c538828f85387`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:26 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:56 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:56 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:56 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:56 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a57a621e2f90878c454c2900fb34b2e03bedcc306a9222c107772613672dfc9`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 1.2 MB (1247569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaa7fbb100f45ffee6750ca12ac096340c2913a360a8beeda5ba4b01d694e28`  
		Last Modified: Mon, 23 Mar 2026 21:33:38 GMT  
		Size: 13.7 MB (13681613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daadcb48818fecaf7145d281b62f72d64c73203df1b5c1cba03554f9ef67687`  
		Last Modified: Mon, 23 Mar 2026 21:33:41 GMT  
		Size: 153.8 MB (153847869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df50c7aa534128b8fa46cf0add79d4ffb8b57bbc4af16455f1339cd50731dda`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.1-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:0ea1489cab0174441d8a6e634f79e701d7a3e677c0919a594d84fc440955add4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e628c3c13542d24af4a7d4661639ed0a14f390a888b038f268dfdcf98e81fc2`

```dockerfile
```

-	Layers:
	-	`sha256:192a7f22b112d9ec1b7ef28fb42ad6fcbdd2f4687d1eaee3e28d6aa445a210f3`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 5.7 MB (5728841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d568062998c575776388d04c7090d619bb718a28c6d2f0001b4ec6e6d8a6bd`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.1-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:20fdc88d1557e233521af22d56acb959c23fb93c1687ca379d2de2979762415c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239965609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05013a90d878f774ed0f6cad6150f890362b5132d3dd76a36d2937df4b65ec87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:23 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:33:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:33:45 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:33:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:33:45 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:33:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9d4a88a3446ee882364a12dd45715592c8caf3941e70428d8bf80a50dc475`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 1.2 MB (1214351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66730a7e2a8e64649282d3e679b71b0794a963394be7f23532455764aaa4fac3`  
		Last Modified: Mon, 23 Mar 2026 21:34:30 GMT  
		Size: 13.7 MB (13671566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d599dc93bd69676edfb560878bfe6d869ac45745b0979d94d2aa4fb664600704`  
		Last Modified: Mon, 23 Mar 2026 21:34:33 GMT  
		Size: 154.7 MB (154747466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692414abc743d668b09fde51ab99e741deb58e289ed9f52ecfb271b5129869a`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.1-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:37f22098bff7f063d035344e295141ddd850fbedaf5a82fb1c7f24a0d448cc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5758123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8956d6025e4be66b9993790b8db707e33f9118b5022cde428d8bd8c35b1941`

```dockerfile
```

-	Layers:
	-	`sha256:09a626197c2b8838253dd647d94b0318b368f11d81cda127086788e043553976`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 5.7 MB (5731638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02b21ea1347601077dbf5d111f5fe8fd9ddeb4bf593027117a925952bfcae826`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:532df5ac9173a7ebb5a9890200818ebb00a4cd93c0d45ed5dbb11b8f7128f8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248989503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083043a4af7a3b001169fa4eb222731b19ebdbbafc21e6003b22609973e60670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:55 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:55 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8884c3f01372d2e4a7474c46a6a3f4c832daab7aa1b99822ebb911326b6420ce`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 1.2 MB (1201503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea814e0687d3f76992f290145881ac774ea1dda23513db4a31b5aaf6921c4d6`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 13.7 MB (13683347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f8618f0b7718f83c70cf3af35e1bf838e322049b898af2e5f6a6b1ae38a27e`  
		Last Modified: Mon, 23 Mar 2026 21:33:44 GMT  
		Size: 154.2 MB (154187137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b24587a07d6009c6736c1b37ccd2617dd2215278bea85ea10c28dd7ceb4d9f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.1-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:c2bddbf5e655a85a72932c684c632cbe432aa824337d46b3d5c5fbf32be2cf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77145a0f19a1617977a8e7073d6dc1b0643b9b715a13d4400fff20c584ace01`

```dockerfile
```

-	Layers:
	-	`sha256:ebfad0586565c6db9343b78119476e7c9e5d0c3abfc1eb96c805c1962b5346d4`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 5.7 MB (5729192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b6450155958226ae3645f5b860b28cf158b635f3e0218e7046a3ddacdb8be3f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.22.1-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:10c95b76ee1638c2b14965868938bf3df60c5420a9c51005d92d61eaf5eec7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250552024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd62e5e5b20c5c893d64d2a0d63d8909b9c128398afc662a97ef4caab16ea690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 21:02:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 21:02:36 GMT
ENV NODE_ENV=production
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:06 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:06 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb0991be587623bd7e5d5529f267aa799aa553646701411b326cf0bedc49f08`  
		Last Modified: Fri, 20 Mar 2026 21:12:35 GMT  
		Size: 1.2 MB (1221347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb6fab34355db319427c08ce5355f0ce4a7847585df335e90fcb1501e579317`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 13.7 MB (13685080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98733d2270747b6d6976cba73d3d17322fefe55018112ba288b4617d60a4cf07`  
		Last Modified: Mon, 23 Mar 2026 21:33:09 GMT  
		Size: 156.9 MB (156906054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913dbdccceed1570268555c5dc113a437a4913eff641d7dd82c7b1f6f15976f`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.22.1-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:a55cf19c79761f21d1352e52d9edb2dda75bd55e2742b5dfd85703eb0502f18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1796ca6388170fe21901544915383a04e469322a542570b61fb8ea477b7d85`

```dockerfile
```

-	Layers:
	-	`sha256:97cd11b0670fff5b1f270a8d33607a18e76d5a242238ee55b75cc6ecaa9ba413`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 5.7 MB (5722666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2b1cc7ccf96fcd3b69663a88f6246e4d6fb638b7d3695a1909fd6180eeb831`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine`

```console
$ docker pull ghost@sha256:4f02907212c3a27dac837a51ace205f13d697c8e5d7ce611cbfb0e4d29551142
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:323e7dc6f9c45075623fbc7b0ab34cb4ed4833b6f4e3a4a654cb68cfc9bdc21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226302331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a12d8a5f0844d7eebaf1a0193281509a2cc5e793babb6f0ac8211a3677e90e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:51 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:15 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:15 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d61e4e317c93f7baa694fdee1e67ab024f703469c8f8e8c9260fe7967a5db`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8c827691e7d79dde0d5895995f8d82a90e4f56d368553bb000e1b8dda8c474`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 928.3 KB (928324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a0a060db6076d19c841d8a37264576eba6722afa2dabe585bee0248a8c434`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 13.7 MB (13681970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ae0207198a3255726cc8557821cfde799fae904dd24a9c36ccee160e7d2989`  
		Last Modified: Mon, 23 Mar 2026 21:32:57 GMT  
		Size: 153.7 MB (153673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d4c9cd4325f2571654f24b325523ef79773d87fb951673c703cfabf3f43aa5`  
		Last Modified: Mon, 23 Mar 2026 21:32:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:ab342386cefb634491e1d5f2506ae9fc03b9c751966a043d5f64c11f0649020a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e573160abafe3de68a1a7e2e1cc47fe0c34936749ecbca49d88a198e4431ebf`

```dockerfile
```

-	Layers:
	-	`sha256:fd8de3eb23b5baac30eec58502a79e393804c6facd7fa1c570ff4a1b63bfdeac`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 3.5 MB (3516840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea448e68e834543f49ce7ae9f41c3656ba6443a98ff48cfd359eadcb2e222fd`  
		Last Modified: Mon, 23 Mar 2026 21:32:53 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:f549dfa0f470bccc18f44ca1a2f507ecafeec4553ab93d465a8d15479a3be0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238420685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8640b018bfaaec34fa1df815b396cf927c2a82a76f28a4d17144abf7fe834b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:35 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:35 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064521911821dc19024bfe059748914160b230bbe68557dd98762deb1b6b43b6`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 891.3 KB (891302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1567db9f8b8a62a578279fda7f78fd3faccaf1d3269de769cafa7d141f80c97`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff613941cfbd284f01e4a2ba730151924641d94d1d7ea7d28a647526d47997b`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 13.7 MB (13682926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2598f4dbb9b4dbcefda013229846cea551c0c45feae80f8ec7ff020211922e`  
		Last Modified: Mon, 23 Mar 2026 21:33:24 GMT  
		Size: 164.8 MB (164807296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b879ea0c6b80ed51f2886e5ca6537a10ba26fbfd50daf9872ccb37d9bef6b0`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:5fbb4a54c0909702a7bbca920d61aa85ae8d4e32876f1e08a1a9c72edbb1f002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ef8a87c4cb31dbacba647a84c613cebfe2b32ffb09339785b694ca7a7b18fa`

```dockerfile
```

-	Layers:
	-	`sha256:2546e7cffbbfdc7c439fa4fb5505c6184fec8500270676ce9f94c6a4da52fe54`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 3.5 MB (3516346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9c9c17adf902326fb0ef26ddad508ee7c1baa23d3dc8d0cf980e7f58b71b52`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine3.23`

```console
$ docker pull ghost@sha256:4f02907212c3a27dac837a51ace205f13d697c8e5d7ce611cbfb0e4d29551142
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:323e7dc6f9c45075623fbc7b0ab34cb4ed4833b6f4e3a4a654cb68cfc9bdc21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226302331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a12d8a5f0844d7eebaf1a0193281509a2cc5e793babb6f0ac8211a3677e90e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:09:25 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:09:25 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:25 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:09:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:09:28 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:51 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:54 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:54 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:15 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:15 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:15 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed87be4595e508c0f2a1ff7a1810938267171d1018a91c41b6dc191f15ca818c`  
		Last Modified: Thu, 05 Mar 2026 21:09:43 GMT  
		Size: 52.1 MB (52071425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c699e235cde407e9ab634f43f63d20708c76c61d2817bd98708fc1aa50c09397`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 1.3 MB (1262116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e1e1c637a965a5768a81fd902f4df05debe64963fcf7c7ed4c5401cc6bcd3`  
		Last Modified: Thu, 05 Mar 2026 21:09:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d61e4e317c93f7baa694fdee1e67ab024f703469c8f8e8c9260fe7967a5db`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 821.9 KB (821895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8c827691e7d79dde0d5895995f8d82a90e4f56d368553bb000e1b8dda8c474`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 928.3 KB (928324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a0a060db6076d19c841d8a37264576eba6722afa2dabe585bee0248a8c434`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 13.7 MB (13681970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ae0207198a3255726cc8557821cfde799fae904dd24a9c36ccee160e7d2989`  
		Last Modified: Mon, 23 Mar 2026 21:32:57 GMT  
		Size: 153.7 MB (153673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d4c9cd4325f2571654f24b325523ef79773d87fb951673c703cfabf3f43aa5`  
		Last Modified: Mon, 23 Mar 2026 21:32:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:ab342386cefb634491e1d5f2506ae9fc03b9c751966a043d5f64c11f0649020a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e573160abafe3de68a1a7e2e1cc47fe0c34936749ecbca49d88a198e4431ebf`

```dockerfile
```

-	Layers:
	-	`sha256:fd8de3eb23b5baac30eec58502a79e393804c6facd7fa1c570ff4a1b63bfdeac`  
		Last Modified: Mon, 23 Mar 2026 21:32:54 GMT  
		Size: 3.5 MB (3516840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea448e68e834543f49ce7ae9f41c3656ba6443a98ff48cfd359eadcb2e222fd`  
		Last Modified: Mon, 23 Mar 2026 21:32:53 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:f549dfa0f470bccc18f44ca1a2f507ecafeec4553ab93d465a8d15479a3be0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238420685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8640b018bfaaec34fa1df815b396cf927c2a82a76f28a4d17144abf7fe834b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 21:40:20 GMT
ENV NODE_VERSION=22.22.1
# Thu, 05 Mar 2026 21:40:20 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a06721f1566c89eb911546dba6309f7da6613dbcc67c0426588b1f39a7210a95" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:20 GMT
ENV YARN_VERSION=1.22.22
# Thu, 05 Mar 2026 21:40:24 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 21:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 21:40:24 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:29:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:29:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:29:28 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:29:28 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:38 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:38 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:35 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:35 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442512ab2742e656cb5a8c7443a3ee91500a6f9dc29096578cf83de1383a805c`  
		Last Modified: Thu, 05 Mar 2026 21:40:43 GMT  
		Size: 52.7 MB (52696772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfef817bf411fcace99981e76ca078620fbc962709bdc7afd6aca7f64454b4c`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a815c829c0e513e4f2bd69aa767e422f08342609bdef13751ac6da4fb1452c5b`  
		Last Modified: Thu, 05 Mar 2026 21:40:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064521911821dc19024bfe059748914160b230bbe68557dd98762deb1b6b43b6`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 891.3 KB (891302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1567db9f8b8a62a578279fda7f78fd3faccaf1d3269de769cafa7d141f80c97`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 881.3 KB (881288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff613941cfbd284f01e4a2ba730151924641d94d1d7ea7d28a647526d47997b`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 13.7 MB (13682926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2598f4dbb9b4dbcefda013229846cea551c0c45feae80f8ec7ff020211922e`  
		Last Modified: Mon, 23 Mar 2026 21:33:24 GMT  
		Size: 164.8 MB (164807296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b879ea0c6b80ed51f2886e5ca6537a10ba26fbfd50daf9872ccb37d9bef6b0`  
		Last Modified: Mon, 23 Mar 2026 21:33:21 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:5fbb4a54c0909702a7bbca920d61aa85ae8d4e32876f1e08a1a9c72edbb1f002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ef8a87c4cb31dbacba647a84c613cebfe2b32ffb09339785b694ca7a7b18fa`

```dockerfile
```

-	Layers:
	-	`sha256:2546e7cffbbfdc7c439fa4fb5505c6184fec8500270676ce9f94c6a4da52fe54`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 3.5 MB (3516346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9c9c17adf902326fb0ef26ddad508ee7c1baa23d3dc8d0cf980e7f58b71b52`  
		Last Modified: Mon, 23 Mar 2026 21:33:20 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:bookworm`

```console
$ docker pull ghost@sha256:1582ff7d419839eea2d5d75867703a6344f0df818f1b31680fe68b2c77940ea7
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

### `ghost:bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:2f9bb6d9eb2bfab9f2dfd77fdd9a821189a3b6d68f1317070ecbc3afb227e4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248679987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e570be6b9273a46c7912f31b3ae1719a8b895f687517bf63e96c538828f85387`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:26 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:56 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:56 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:56 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:56 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a57a621e2f90878c454c2900fb34b2e03bedcc306a9222c107772613672dfc9`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 1.2 MB (1247569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaa7fbb100f45ffee6750ca12ac096340c2913a360a8beeda5ba4b01d694e28`  
		Last Modified: Mon, 23 Mar 2026 21:33:38 GMT  
		Size: 13.7 MB (13681613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daadcb48818fecaf7145d281b62f72d64c73203df1b5c1cba03554f9ef67687`  
		Last Modified: Mon, 23 Mar 2026 21:33:41 GMT  
		Size: 153.8 MB (153847869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df50c7aa534128b8fa46cf0add79d4ffb8b57bbc4af16455f1339cd50731dda`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:0ea1489cab0174441d8a6e634f79e701d7a3e677c0919a594d84fc440955add4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e628c3c13542d24af4a7d4661639ed0a14f390a888b038f268dfdcf98e81fc2`

```dockerfile
```

-	Layers:
	-	`sha256:192a7f22b112d9ec1b7ef28fb42ad6fcbdd2f4687d1eaee3e28d6aa445a210f3`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 5.7 MB (5728841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d568062998c575776388d04c7090d619bb718a28c6d2f0001b4ec6e6d8a6bd`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:20fdc88d1557e233521af22d56acb959c23fb93c1687ca379d2de2979762415c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239965609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05013a90d878f774ed0f6cad6150f890362b5132d3dd76a36d2937df4b65ec87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:23 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:33:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:33:45 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:33:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:33:45 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:33:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9d4a88a3446ee882364a12dd45715592c8caf3941e70428d8bf80a50dc475`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 1.2 MB (1214351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66730a7e2a8e64649282d3e679b71b0794a963394be7f23532455764aaa4fac3`  
		Last Modified: Mon, 23 Mar 2026 21:34:30 GMT  
		Size: 13.7 MB (13671566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d599dc93bd69676edfb560878bfe6d869ac45745b0979d94d2aa4fb664600704`  
		Last Modified: Mon, 23 Mar 2026 21:34:33 GMT  
		Size: 154.7 MB (154747466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692414abc743d668b09fde51ab99e741deb58e289ed9f52ecfb271b5129869a`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:37f22098bff7f063d035344e295141ddd850fbedaf5a82fb1c7f24a0d448cc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5758123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8956d6025e4be66b9993790b8db707e33f9118b5022cde428d8bd8c35b1941`

```dockerfile
```

-	Layers:
	-	`sha256:09a626197c2b8838253dd647d94b0318b368f11d81cda127086788e043553976`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 5.7 MB (5731638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02b21ea1347601077dbf5d111f5fe8fd9ddeb4bf593027117a925952bfcae826`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:532df5ac9173a7ebb5a9890200818ebb00a4cd93c0d45ed5dbb11b8f7128f8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248989503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083043a4af7a3b001169fa4eb222731b19ebdbbafc21e6003b22609973e60670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:55 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:55 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8884c3f01372d2e4a7474c46a6a3f4c832daab7aa1b99822ebb911326b6420ce`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 1.2 MB (1201503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea814e0687d3f76992f290145881ac774ea1dda23513db4a31b5aaf6921c4d6`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 13.7 MB (13683347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f8618f0b7718f83c70cf3af35e1bf838e322049b898af2e5f6a6b1ae38a27e`  
		Last Modified: Mon, 23 Mar 2026 21:33:44 GMT  
		Size: 154.2 MB (154187137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b24587a07d6009c6736c1b37ccd2617dd2215278bea85ea10c28dd7ceb4d9f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:c2bddbf5e655a85a72932c684c632cbe432aa824337d46b3d5c5fbf32be2cf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77145a0f19a1617977a8e7073d6dc1b0643b9b715a13d4400fff20c584ace01`

```dockerfile
```

-	Layers:
	-	`sha256:ebfad0586565c6db9343b78119476e7c9e5d0c3abfc1eb96c805c1962b5346d4`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 5.7 MB (5729192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b6450155958226ae3645f5b860b28cf158b635f3e0218e7046a3ddacdb8be3f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:10c95b76ee1638c2b14965868938bf3df60c5420a9c51005d92d61eaf5eec7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250552024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd62e5e5b20c5c893d64d2a0d63d8909b9c128398afc662a97ef4caab16ea690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 21:02:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 21:02:36 GMT
ENV NODE_ENV=production
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:06 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:06 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb0991be587623bd7e5d5529f267aa799aa553646701411b326cf0bedc49f08`  
		Last Modified: Fri, 20 Mar 2026 21:12:35 GMT  
		Size: 1.2 MB (1221347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb6fab34355db319427c08ce5355f0ce4a7847585df335e90fcb1501e579317`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 13.7 MB (13685080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98733d2270747b6d6976cba73d3d17322fefe55018112ba288b4617d60a4cf07`  
		Last Modified: Mon, 23 Mar 2026 21:33:09 GMT  
		Size: 156.9 MB (156906054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913dbdccceed1570268555c5dc113a437a4913eff641d7dd82c7b1f6f15976f`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:a55cf19c79761f21d1352e52d9edb2dda75bd55e2742b5dfd85703eb0502f18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1796ca6388170fe21901544915383a04e469322a542570b61fb8ea477b7d85`

```dockerfile
```

-	Layers:
	-	`sha256:97cd11b0670fff5b1f270a8d33607a18e76d5a242238ee55b75cc6ecaa9ba413`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 5.7 MB (5722666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2b1cc7ccf96fcd3b69663a88f6246e4d6fb638b7d3695a1909fd6180eeb831`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:latest`

```console
$ docker pull ghost@sha256:1582ff7d419839eea2d5d75867703a6344f0df818f1b31680fe68b2c77940ea7
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

### `ghost:latest` - linux; amd64

```console
$ docker pull ghost@sha256:2f9bb6d9eb2bfab9f2dfd77fdd9a821189a3b6d68f1317070ecbc3afb227e4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248679987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e570be6b9273a46c7912f31b3ae1719a8b895f687517bf63e96c538828f85387`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:45:37 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:37 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:45:50 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:50 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:26 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:26 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:56 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:56 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:56 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:56 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260c4bd6721aa9cf70355d170f8cad17e2194840a22c0bc9afae1789fb6a731`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb89e70384b59a4860d1f1c56f6f91043d2f8e1394bd9799d7d576f1199fd40`  
		Last Modified: Mon, 16 Mar 2026 22:46:06 GMT  
		Size: 49.9 MB (49949707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b65622f4612343e8373dca1cc9358d43b393ded920a92da897b8a82b5d51139`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 1.7 MB (1712674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07293921e5871b5544e13097dc0c65d28920dc8a5f94216e2af10843f7986e`  
		Last Modified: Mon, 16 Mar 2026 22:46:04 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a57a621e2f90878c454c2900fb34b2e03bedcc306a9222c107772613672dfc9`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 1.2 MB (1247569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaa7fbb100f45ffee6750ca12ac096340c2913a360a8beeda5ba4b01d694e28`  
		Last Modified: Mon, 23 Mar 2026 21:33:38 GMT  
		Size: 13.7 MB (13681613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daadcb48818fecaf7145d281b62f72d64c73203df1b5c1cba03554f9ef67687`  
		Last Modified: Mon, 23 Mar 2026 21:33:41 GMT  
		Size: 153.8 MB (153847869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df50c7aa534128b8fa46cf0add79d4ffb8b57bbc4af16455f1339cd50731dda`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:0ea1489cab0174441d8a6e634f79e701d7a3e677c0919a594d84fc440955add4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e628c3c13542d24af4a7d4661639ed0a14f390a888b038f268dfdcf98e81fc2`

```dockerfile
```

-	Layers:
	-	`sha256:192a7f22b112d9ec1b7ef28fb42ad6fcbdd2f4687d1eaee3e28d6aa445a210f3`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 5.7 MB (5728841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d568062998c575776388d04c7090d619bb718a28c6d2f0001b4ec6e6d8a6bd`  
		Last Modified: Mon, 23 Mar 2026 21:33:37 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:20fdc88d1557e233521af22d56acb959c23fb93c1687ca379d2de2979762415c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239965609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05013a90d878f774ed0f6cad6150f890362b5132d3dd76a36d2937df4b65ec87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:31:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:31:44 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:44 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:31:57 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:31:57 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:23 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:23 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:35 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:35 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:33:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:33:45 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:33:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:33:45 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:33:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642f17477f6a151e56a8f98e020c651ec7cbfe0558ba44f430bfec400cce9e7b`  
		Last Modified: Mon, 16 Mar 2026 23:32:10 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a6cd9cc49af1802bdea56f1cf543293d2262db12f823e2a6214a4b8e0207f`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 44.7 MB (44673757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403610b0e20878b48323c7e97dfa4ded18a0aa7ea5bbe36862d303e17a0804ee`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 1.7 MB (1712799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e08e58209bacd85ac5ac5ad6f147945d3794cb9f882214838817bfc20504e5`  
		Last Modified: Mon, 16 Mar 2026 23:32:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9d4a88a3446ee882364a12dd45715592c8caf3941e70428d8bf80a50dc475`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 1.2 MB (1214351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66730a7e2a8e64649282d3e679b71b0794a963394be7f23532455764aaa4fac3`  
		Last Modified: Mon, 23 Mar 2026 21:34:30 GMT  
		Size: 13.7 MB (13671566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d599dc93bd69676edfb560878bfe6d869ac45745b0979d94d2aa4fb664600704`  
		Last Modified: Mon, 23 Mar 2026 21:34:33 GMT  
		Size: 154.7 MB (154747466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692414abc743d668b09fde51ab99e741deb58e289ed9f52ecfb271b5129869a`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:37f22098bff7f063d035344e295141ddd850fbedaf5a82fb1c7f24a0d448cc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5758123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8956d6025e4be66b9993790b8db707e33f9118b5022cde428d8bd8c35b1941`

```dockerfile
```

-	Layers:
	-	`sha256:09a626197c2b8838253dd647d94b0318b368f11d81cda127086788e043553976`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 5.7 MB (5731638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02b21ea1347601077dbf5d111f5fe8fd9ddeb4bf593027117a925952bfcae826`  
		Last Modified: Mon, 23 Mar 2026 21:34:29 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:532df5ac9173a7ebb5a9890200818ebb00a4cd93c0d45ed5dbb11b8f7128f8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248989503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083043a4af7a3b001169fa4eb222731b19ebdbbafc21e6003b22609973e60670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:27 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 22:47:47 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:47:47 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 22:48:00 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:48:00 GMT
CMD ["node"]
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GOSU_VERSION=1.19
# Mon, 23 Mar 2026 21:30:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 23 Mar 2026 21:30:03 GMT
ENV NODE_ENV=production
# Mon, 23 Mar 2026 21:30:03 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:30:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:30:13 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:54 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:55 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:55 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809e72c1c0ebba2150666e12a9c7624e798cf861e9a47083029ba1191e2835c`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d625b2c5e074296f128b5abe0398dd200796588b1b013e45bae0d00904677f6`  
		Last Modified: Mon, 16 Mar 2026 22:48:16 GMT  
		Size: 50.1 MB (50084474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb87eadb6bc181ae0593382b798e87ca11438eab7a7c53a11ec8da728fd1099`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 1.7 MB (1712651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dd6d841b8174b81e59136efc9866b6ecb07b716cb3aa037e9c9f56fb54fb3`  
		Last Modified: Mon, 16 Mar 2026 22:48:15 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8884c3f01372d2e4a7474c46a6a3f4c832daab7aa1b99822ebb911326b6420ce`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 1.2 MB (1201503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea814e0687d3f76992f290145881ac774ea1dda23513db4a31b5aaf6921c4d6`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 13.7 MB (13683347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f8618f0b7718f83c70cf3af35e1bf838e322049b898af2e5f6a6b1ae38a27e`  
		Last Modified: Mon, 23 Mar 2026 21:33:44 GMT  
		Size: 154.2 MB (154187137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b24587a07d6009c6736c1b37ccd2617dd2215278bea85ea10c28dd7ceb4d9f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:c2bddbf5e655a85a72932c684c632cbe432aa824337d46b3d5c5fbf32be2cf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77145a0f19a1617977a8e7073d6dc1b0643b9b715a13d4400fff20c584ace01`

```dockerfile
```

-	Layers:
	-	`sha256:ebfad0586565c6db9343b78119476e7c9e5d0c3abfc1eb96c805c1962b5346d4`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 5.7 MB (5729192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b6450155958226ae3645f5b860b28cf158b635f3e0218e7046a3ddacdb8be3f`  
		Last Modified: Mon, 23 Mar 2026 21:33:40 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:10c95b76ee1638c2b14965868938bf3df60c5420a9c51005d92d61eaf5eec7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250552024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd62e5e5b20c5c893d64d2a0d63d8909b9c128398afc662a97ef4caab16ea690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:52:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV NODE_VERSION=22.22.1
# Mon, 16 Mar 2026 23:52:24 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:24 GMT
ENV YARN_VERSION=1.22.22
# Mon, 16 Mar 2026 23:52:38 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:52:38 GMT
CMD ["node"]
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 21:02:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 21:02:36 GMT
ENV NODE_ENV=production
# Fri, 20 Mar 2026 21:02:36 GMT
ENV GHOST_CLI_VERSION=1.28.6
# Mon, 23 Mar 2026 21:29:47 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 23 Mar 2026 21:29:47 GMT
ENV GHOST_VERSION=6.22.1
# Mon, 23 Mar 2026 21:32:05 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
WORKDIR /var/lib/ghost
# Mon, 23 Mar 2026 21:32:06 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 23 Mar 2026 21:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 21:32:06 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 23 Mar 2026 21:32:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2bdde69e23d6d54d1d034544fd9d98cc1abac77cfe9ab7f5970674e204`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc698d0971dc9eb9e0c348e78b8690a7d5926511104d73ca05b5e3558b4fdc`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 50.1 MB (50131045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2d48434ac03a026788daead831b5e9a2a25c5ac31e0e2b87cfed9f73cee3`  
		Last Modified: Mon, 16 Mar 2026 23:53:06 GMT  
		Size: 1.7 MB (1712653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7389caaecb97465749b65e81d014dd8868c1fd294f65281841e299909412eb9a`  
		Last Modified: Mon, 16 Mar 2026 23:53:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb0991be587623bd7e5d5529f267aa799aa553646701411b326cf0bedc49f08`  
		Last Modified: Fri, 20 Mar 2026 21:12:35 GMT  
		Size: 1.2 MB (1221347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb6fab34355db319427c08ce5355f0ce4a7847585df335e90fcb1501e579317`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 13.7 MB (13685080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98733d2270747b6d6976cba73d3d17322fefe55018112ba288b4617d60a4cf07`  
		Last Modified: Mon, 23 Mar 2026 21:33:09 GMT  
		Size: 156.9 MB (156906054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913dbdccceed1570268555c5dc113a437a4913eff641d7dd82c7b1f6f15976f`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:a55cf19c79761f21d1352e52d9edb2dda75bd55e2742b5dfd85703eb0502f18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1796ca6388170fe21901544915383a04e469322a542570b61fb8ea477b7d85`

```dockerfile
```

-	Layers:
	-	`sha256:97cd11b0670fff5b1f270a8d33607a18e76d5a242238ee55b75cc6ecaa9ba413`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 5.7 MB (5722666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2b1cc7ccf96fcd3b69663a88f6246e4d6fb638b7d3695a1909fd6180eeb831`  
		Last Modified: Mon, 23 Mar 2026 21:33:06 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

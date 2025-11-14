<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:5`](#ghost5)
-	[`ghost:5-alpine`](#ghost5-alpine)
-	[`ghost:5-alpine3.22`](#ghost5-alpine322)
-	[`ghost:5-bookworm`](#ghost5-bookworm)
-	[`ghost:5.130`](#ghost5130)
-	[`ghost:5.130-alpine`](#ghost5130-alpine)
-	[`ghost:5.130-alpine3.22`](#ghost5130-alpine322)
-	[`ghost:5.130-bookworm`](#ghost5130-bookworm)
-	[`ghost:5.130.5`](#ghost51305)
-	[`ghost:5.130.5-alpine`](#ghost51305-alpine)
-	[`ghost:5.130.5-alpine3.22`](#ghost51305-alpine322)
-	[`ghost:5.130.5-bookworm`](#ghost51305-bookworm)
-	[`ghost:6`](#ghost6)
-	[`ghost:6-alpine`](#ghost6-alpine)
-	[`ghost:6-alpine3.22`](#ghost6-alpine322)
-	[`ghost:6-bookworm`](#ghost6-bookworm)
-	[`ghost:6.8`](#ghost68)
-	[`ghost:6.8-alpine`](#ghost68-alpine)
-	[`ghost:6.8-alpine3.22`](#ghost68-alpine322)
-	[`ghost:6.8-bookworm`](#ghost68-bookworm)
-	[`ghost:6.8.0`](#ghost680)
-	[`ghost:6.8.0-alpine`](#ghost680-alpine)
-	[`ghost:6.8.0-alpine3.22`](#ghost680-alpine322)
-	[`ghost:6.8.0-bookworm`](#ghost680-bookworm)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:alpine3.22`](#ghostalpine322)
-	[`ghost:bookworm`](#ghostbookworm)
-	[`ghost:latest`](#ghostlatest)

## `ghost:5`

```console
$ docker pull ghost@sha256:337ce3180f977caa1a6c0fcd725395994cd580f622bfad1b2e2062cf7642a5cc
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

### `ghost:5` - linux; amd64

```console
$ docker pull ghost@sha256:f85733f3cbc898d36de4088f2fda14a125f8a49532ec00c7434cb8ea0e421f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb803bfa37a1461f5c31b8082c18f7b30fb4cafa2d430641d448228a6d4e34ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:34:32 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:34:32 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:32 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:34:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:43 GMT
CMD ["node"]
# Tue, 04 Nov 2025 04:33:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 04:33:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 04:33:50 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 04:33:50 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 04:34:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 04:35:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 04:35:07 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 04:35:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 04:35:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:35:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:35:07 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 04:35:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f707883943caee6170d1c96b0e24f29b11404bd9817e8e658e8c24898f94807`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9be599d8cff95c94bc0036ba643b354bfb691616e6f582ee79e08a20071764e`  
		Last Modified: Tue, 04 Nov 2025 00:35:04 GMT  
		Size: 41.0 MB (40977842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561299ddc92fb2324b06da8e6e176820a7eba31727bb4bc1cb1a28403ff4db12`  
		Last Modified: Tue, 04 Nov 2025 00:35:02 GMT  
		Size: 1.7 MB (1712619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7eb6b5a2b17e46a979515b9e341cce1eafc9b6035d440d435715fbb77690bb`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864aed93e665e6fa26d34620ea863882b848dc24e86f0fe197cdced4114e4562`  
		Last Modified: Tue, 04 Nov 2025 04:35:47 GMT  
		Size: 1.2 MB (1247537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba6c8fd4f450c1f7457c81998f7dd13f3010e3a4113093b112b454a1e2d09a4`  
		Last Modified: Tue, 04 Nov 2025 04:35:48 GMT  
		Size: 11.1 MB (11094147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3d3dff4aaa867d1ae255c80633027f39d66e5281984beb46805075f78e11a5`  
		Last Modified: Tue, 04 Nov 2025 04:35:54 GMT  
		Size: 118.0 MB (118018049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d29e5f38b1e0fa7e0f98cae6416943814b9a57577170b459e4451f1db9f44d`  
		Last Modified: Tue, 04 Nov 2025 04:35:47 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:f4217b269e6c02f3b0044770a218ece6b4f9e62e2f2343af1989d7fb9fa0927f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f37142f2048af11deff44531397262046cfa9a752576896fac6401fdc4892e`

```dockerfile
```

-	Layers:
	-	`sha256:8c0305204fbc4eb1195f4a4532034b13bf62f90401195df4f47e23ef7aaf052c`  
		Last Modified: Tue, 04 Nov 2025 10:45:27 GMT  
		Size: 5.5 MB (5543181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4631011bb1a1306639afdeeb7e8acfe2dfbec54142e99360f5adcc478982daa3`  
		Last Modified: Tue, 04 Nov 2025 10:45:28 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:d54af2f62dbe59d10c76ec8b4c87eda9ba3e2a80e130a1270eaa7fd4b094048f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195612293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e008e162f1176295a864de55fd1777a3adbff9626cc579c97fbcce62b8501f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:46:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:47:03 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:47:03 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:47:03 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:47:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:47:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:47:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:47:15 GMT
CMD ["node"]
# Tue, 04 Nov 2025 02:43:46 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 02:43:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 02:43:46 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 02:43:46 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 02:44:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 02:46:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 02:46:49 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 02:46:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 02:46:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:46:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:46:49 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 02:46:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93c37c1fd1b7f4d09c483f03a2a845c305e3e3ecc99b3b52d68d46608ebb3f`  
		Last Modified: Tue, 04 Nov 2025 00:47:34 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7f2cf1babca77eeed4ac645ee2ed904d57e7ee6a13ff624054af478867074d`  
		Last Modified: Tue, 04 Nov 2025 00:47:38 GMT  
		Size: 37.1 MB (37064306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488f9e73958b5133b77535cce142f45578b4297a9b3554e3f83c569f3363b2f`  
		Last Modified: Tue, 04 Nov 2025 00:47:34 GMT  
		Size: 1.7 MB (1712823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb0f6234b40d280dd577f5ff6c58d1b026b669fdb3e89d6e96f2d5a1efcca7f`  
		Last Modified: Tue, 04 Nov 2025 00:47:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e8191b4d8b62dbbdb3ef3d4a6b899a6fede17cb071db5d2bbd145f29b88bd0`  
		Last Modified: Tue, 04 Nov 2025 02:47:32 GMT  
		Size: 1.2 MB (1214355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3102d25ad11605635394177f33ad305073fc8c0267601aadc4a9cbd9a68212`  
		Last Modified: Tue, 04 Nov 2025 02:47:33 GMT  
		Size: 11.1 MB (11094829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deeef39e9f4c1c4d9cf2263beb1ed290d522127aab93d27721ff9806f0a2fe5a`  
		Last Modified: Tue, 04 Nov 2025 02:47:44 GMT  
		Size: 120.6 MB (120587524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d66cc2862765c4676c6164d0f4ed12303ff5421ad0d8be8f792f1cd1b87ae7`  
		Last Modified: Tue, 04 Nov 2025 02:47:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:940a9180000c1e68107a92ebdcfabeb0f181107cd9aa1df4cca5e768eb4ae1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d3cecb5fb064dc47a02da45dbfa06e6ec6cc4d8adb55e0694a81189ff25588`

```dockerfile
```

-	Layers:
	-	`sha256:d03259ddf9f5bea23fc228da9cad31e09474df6b009d025a60263281d9e6e3fa`  
		Last Modified: Tue, 04 Nov 2025 10:45:32 GMT  
		Size: 5.5 MB (5545960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bef53d686d15b6e964d4fa9cf4d4cea8735c5702804503b0776dc18ab6bfd45`  
		Last Modified: Tue, 04 Nov 2025 10:45:33 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b84f862c680ac2c30d07bc0b6c7ebdce04d4a85e0fd7045807073e95cc3a88e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201178174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3c609ac0e52a737db94f0a2a90d598558a4f2a5fd52f4c64ff045464a9d384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:23 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:35:42 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:35:42 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:42 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:35:53 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:35:53 GMT
CMD ["node"]
# Tue, 04 Nov 2025 01:48:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 01:48:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 01:48:51 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 01:48:51 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 01:49:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 01:50:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 01:50:19 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 01:50:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 01:50:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:50:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:50:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 01:50:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e3e431f7a520df14961d4498593d85568abcee7af80df09bfb1ecaef7cd45`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd1f8ab98ef1e2152eab9b695ec2f87db4d02435d64fdec15bd10a153ff849`  
		Last Modified: Tue, 04 Nov 2025 00:36:20 GMT  
		Size: 40.9 MB (40939662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaa03f4a05ff40bcfbe40175a2dbd854534498b254584994ed85d776bb55587`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 1.7 MB (1712633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6570b58c3e47b958ae4b68f789413ade8fe66580a20c717b3cb1e69f0c133ebf`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663ae620ac190c68e5d83a83b3d33b0eb2eb423a03fac16114cd3cd12cc5019f`  
		Last Modified: Tue, 04 Nov 2025 01:51:03 GMT  
		Size: 1.2 MB (1201430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9c0870ca41dfc91a0e2a298cdc47e8114d6f3d09c14d764b2d753f5f0670ce`  
		Last Modified: Tue, 04 Nov 2025 01:51:03 GMT  
		Size: 11.1 MB (11094919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602531b4420813b49243982ad8a1c2a9549dbae632743b32cb5a9805b2403887`  
		Last Modified: Tue, 04 Nov 2025 01:51:18 GMT  
		Size: 118.1 MB (118122828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295d0e4df7a9fe45640c39d05aa3a0c0eaaf7a3087e6211d12a3e53d0e9b6312`  
		Last Modified: Tue, 04 Nov 2025 01:51:02 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:445ef3bc796bab18ada3fba661be331b721a771a43efdc88647eb5d116d4c68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5569425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4965280d091d4279629434307cdbaf3fb262b9134a9a4d73aab1897800946f`

```dockerfile
```

-	Layers:
	-	`sha256:067f8b997a5e51ef10a4601a130dfc95344c8ee4b8b4a912a5304279072e0562`  
		Last Modified: Tue, 04 Nov 2025 10:45:37 GMT  
		Size: 5.5 MB (5543508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:321b4338d423ea63134b074ba90c5d4d27bc35d8d7a43c0b0c1ddcc801008c85`  
		Last Modified: Tue, 04 Nov 2025 10:45:38 GMT  
		Size: 25.9 KB (25917 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; s390x

```console
$ docker pull ghost@sha256:fedc92789cc63ec80586657b88fa4c694f5ef240cd4f4a2b6c1688440c7a4439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204802905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c301e77ea9647ac3183392844f94ef4ebc65b70ae40551ea9eadc7d1b9625a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:33:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 03:37:01 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 03:37:01 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:37:01 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 03:37:10 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:37:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:37:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:37:10 GMT
CMD ["node"]
# Tue, 04 Nov 2025 13:34:35 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 13:34:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 13:34:35 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 13:34:35 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 13:34:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 13:37:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 13:37:13 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 13:37:13 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 13:37:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 13:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 13:37:13 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 13:37:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b483b0df66cd8c70ba210c61fdc3840348da24bad86177f3799a15a254e527`  
		Last Modified: Tue, 04 Nov 2025 03:34:01 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a391e545ed0d8aeddbbfdf6c58840bd79044b2d7724a7f9e2f4b25f94cd446`  
		Last Modified: Tue, 04 Nov 2025 03:37:41 GMT  
		Size: 41.2 MB (41222577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff94fd9f029756b1291b5b34bfc358a41e9c02a77d415cf91c92e6480c8cc12`  
		Last Modified: Tue, 04 Nov 2025 03:37:39 GMT  
		Size: 1.7 MB (1712621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb828a655db1ab796ec4ec301dbddaed50020b282af492e0ad200dcd1a7f9a7`  
		Last Modified: Tue, 04 Nov 2025 03:37:39 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f328b3f0fc2f5ec6a0ce9d45ffce274cdc93a98a55cd8eaaa4d1cb295fb11a`  
		Last Modified: Tue, 04 Nov 2025 13:38:12 GMT  
		Size: 1.2 MB (1221301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84250905d6e664f6e19a3907889c1832e155c4a9e639f732621d0ad78b5eea0f`  
		Last Modified: Tue, 04 Nov 2025 13:38:15 GMT  
		Size: 11.1 MB (11093207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaf51cd926003ef4b173028a768cbd8235b7fab10f8364c526e52155d74609b`  
		Last Modified: Tue, 04 Nov 2025 13:38:22 GMT  
		Size: 122.7 MB (122664325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002ebcdf1e703e7b6e8e6dedf4cff0aba49d24404fce1007cd77b34af1011f7c`  
		Last Modified: Tue, 04 Nov 2025 13:38:12 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:aea28f5f061e7e1fe6c72475dc569a1ff0dcf919d99e365cb48cd601995c2908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7f4f9dbf6f2371841cfe530c36b8341ca0772822038bd3983ca67428f477bf`

```dockerfile
```

-	Layers:
	-	`sha256:7964a06228d679e34749309df911e4f993cfdb332d28c9b0117e17e9a52c4197`  
		Last Modified: Tue, 04 Nov 2025 16:45:31 GMT  
		Size: 5.5 MB (5537004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9aa56bb8d72e1ec060d747be18da6e100963612bda5035ca87306b345192c5d`  
		Last Modified: Tue, 04 Nov 2025 16:45:32 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-alpine`

```console
$ docker pull ghost@sha256:6cca0c2a8a2ca5f57e31bf311e8c35b570be0b0c2451c9c37bea55197bdfeb68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:0f70a24b1ba6a1d3997eaf4853a6e6f6d6fafb0446c28f3deeaf3a01252423f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175511698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68920e05396cd4669b7e3c46d22a38fb4333b55009f4ea79fa4b6209db38440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:24 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:14:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:14:26 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:14:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:14:26 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:14:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e45a9660cfaebbbac9bba98180aa28b3966b7f2462d132c46f51a1f5b25a64`  
		Last Modified: Tue, 21 Oct 2025 20:19:28 GMT  
		Size: 42.8 MB (42750841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74e4ed823e9560b3fe51c0cab47dbfdfc4b12453604319408ec58708fb9e720`  
		Last Modified: Tue, 21 Oct 2025 20:19:17 GMT  
		Size: 1.3 MB (1260590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04d522c98fe12816b2bcddf8413fca73645f8fa60f287c672f58bcc7f0fa38`  
		Last Modified: Tue, 21 Oct 2025 20:19:16 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0f9a897060feb550287b8d83fcf4ee55da3c30f54db1edf978b006db787df`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 777.0 KB (777045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b382b367f507fc850a39a16fec12749f6c1306dc08e0e4f5d9fb4e9fb87140`  
		Last Modified: Mon, 03 Nov 2025 23:15:08 GMT  
		Size: 923.4 KB (923439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4892805e65559d25032860f128b6ffde24688439b15eafae4582e7433248835`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be658ce9c8e59f7aa9d714b669e868cc97bb892900145e917445a00f7684af`  
		Last Modified: Mon, 03 Nov 2025 23:15:09 GMT  
		Size: 11.1 MB (11093048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67e9dd34d742b7cb05cf61410a70c7992f27db78d903721c0c4cb0550b4883`  
		Last Modified: Mon, 03 Nov 2025 23:15:17 GMT  
		Size: 114.9 MB (114903085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa3dd720a5026dbd84f0306d99be03e7e0f6481b674c2a664c60743d5b0bf5`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:0705a01a45b41466c233e6ff85abb3245f22f31baa322462468a6c9d259c7ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5c4812ee7cd0ae829317bd459870791c1165f3b1ece1398199ae4792524700`

```dockerfile
```

-	Layers:
	-	`sha256:1210e51ac71ad4e5f3362abb7b760cf9634edaa2629be743b66e7e65cc2bf36d`  
		Last Modified: Tue, 04 Nov 2025 01:45:24 GMT  
		Size: 3.3 MB (3330079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e4429e809841d6839249a064f9f674748ca2445fab5bbf04eeabf3c5053ace`  
		Last Modified: Tue, 04 Nov 2025 01:45:25 GMT  
		Size: 28.3 KB (28295 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:86bf1443622143bb16bee447fe4c778ad3e965699ee809c01355752173c0923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186152453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3311524bf8d21f721e8381834f51617e7085c55d1156e168336a952037c0819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:41 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:15:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:15:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:15:00 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:15:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae67534e7d0aa8a27cfb7e3ecb9727f2ce2a6dd5b721d5392c27b91fc68b7f13`  
		Last Modified: Tue, 21 Oct 2025 19:27:20 GMT  
		Size: 42.4 MB (42425867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf56a7feaf43fe338cd74317fda62608ec88dfd616dd5bff62f6f11b631692`  
		Last Modified: Tue, 21 Oct 2025 19:27:16 GMT  
		Size: 1.3 MB (1260570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dae84293a5e75bd15077274b31b14eaec6c0fc94e035b36febae220198d1f2`  
		Last Modified: Tue, 21 Oct 2025 19:27:15 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a9c55bf6a0924e65b32510d0961685bdd8d8f2b10c2db7dd7c96bdd51bf6a9`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 838.6 KB (838585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6208bc17bacacf9b675576e3a0f1ea6703a538aa99a36a8afc4f265ad6606fd4`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e145e2590cb18e81ffe8ac9d21e865b79a70aae4f5cf913d72227d6b5a0c89f`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5e151584a8a323c8c95a64b09e39e356af36f4eaafda1e33ccbd47f82ccb9c`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 11.1 MB (11094690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea721408dbea49d2025fa1a9c571d38cb1fc8f275fc6505f5dad38b4f7f0f44`  
		Last Modified: Mon, 03 Nov 2025 23:16:00 GMT  
		Size: 125.5 MB (125517109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df139f51032436062d10fd724eba3c899f0f3c8bdb77226d7140ecfcc55e6308`  
		Last Modified: Mon, 03 Nov 2025 23:15:47 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:d3def10dd533d48e2cbbf4453012f2197ed4d09a6cfb48880f830a1436e526e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e2fa9bacdd7216a338861d1c288ae6ee8a60f4fc28c1105ec3906ebeb554a2`

```dockerfile
```

-	Layers:
	-	`sha256:32d63c33bb3db7b0d81adf8e25e21c55071e4fe60e7e4a74d6191983d7d6b88b`  
		Last Modified: Tue, 04 Nov 2025 01:45:29 GMT  
		Size: 3.3 MB (3330211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abbb7369c2dac9f8713988834f81b90112f90d7083f3f254112a5711ac640346`  
		Last Modified: Tue, 04 Nov 2025 01:45:30 GMT  
		Size: 28.5 KB (28483 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-alpine3.22`

```console
$ docker pull ghost@sha256:6cca0c2a8a2ca5f57e31bf311e8c35b570be0b0c2451c9c37bea55197bdfeb68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5-alpine3.22` - linux; amd64

```console
$ docker pull ghost@sha256:0f70a24b1ba6a1d3997eaf4853a6e6f6d6fafb0446c28f3deeaf3a01252423f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175511698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68920e05396cd4669b7e3c46d22a38fb4333b55009f4ea79fa4b6209db38440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:24 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:14:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:14:26 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:14:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:14:26 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:14:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e45a9660cfaebbbac9bba98180aa28b3966b7f2462d132c46f51a1f5b25a64`  
		Last Modified: Tue, 21 Oct 2025 20:19:28 GMT  
		Size: 42.8 MB (42750841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74e4ed823e9560b3fe51c0cab47dbfdfc4b12453604319408ec58708fb9e720`  
		Last Modified: Tue, 21 Oct 2025 20:19:17 GMT  
		Size: 1.3 MB (1260590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04d522c98fe12816b2bcddf8413fca73645f8fa60f287c672f58bcc7f0fa38`  
		Last Modified: Tue, 21 Oct 2025 20:19:16 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0f9a897060feb550287b8d83fcf4ee55da3c30f54db1edf978b006db787df`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 777.0 KB (777045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b382b367f507fc850a39a16fec12749f6c1306dc08e0e4f5d9fb4e9fb87140`  
		Last Modified: Mon, 03 Nov 2025 23:15:08 GMT  
		Size: 923.4 KB (923439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4892805e65559d25032860f128b6ffde24688439b15eafae4582e7433248835`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be658ce9c8e59f7aa9d714b669e868cc97bb892900145e917445a00f7684af`  
		Last Modified: Mon, 03 Nov 2025 23:15:09 GMT  
		Size: 11.1 MB (11093048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67e9dd34d742b7cb05cf61410a70c7992f27db78d903721c0c4cb0550b4883`  
		Last Modified: Mon, 03 Nov 2025 23:15:17 GMT  
		Size: 114.9 MB (114903085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa3dd720a5026dbd84f0306d99be03e7e0f6481b674c2a664c60743d5b0bf5`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:0705a01a45b41466c233e6ff85abb3245f22f31baa322462468a6c9d259c7ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5c4812ee7cd0ae829317bd459870791c1165f3b1ece1398199ae4792524700`

```dockerfile
```

-	Layers:
	-	`sha256:1210e51ac71ad4e5f3362abb7b760cf9634edaa2629be743b66e7e65cc2bf36d`  
		Last Modified: Tue, 04 Nov 2025 01:45:24 GMT  
		Size: 3.3 MB (3330079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e4429e809841d6839249a064f9f674748ca2445fab5bbf04eeabf3c5053ace`  
		Last Modified: Tue, 04 Nov 2025 01:45:25 GMT  
		Size: 28.3 KB (28295 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:86bf1443622143bb16bee447fe4c778ad3e965699ee809c01355752173c0923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186152453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3311524bf8d21f721e8381834f51617e7085c55d1156e168336a952037c0819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:41 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:15:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:15:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:15:00 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:15:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae67534e7d0aa8a27cfb7e3ecb9727f2ce2a6dd5b721d5392c27b91fc68b7f13`  
		Last Modified: Tue, 21 Oct 2025 19:27:20 GMT  
		Size: 42.4 MB (42425867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf56a7feaf43fe338cd74317fda62608ec88dfd616dd5bff62f6f11b631692`  
		Last Modified: Tue, 21 Oct 2025 19:27:16 GMT  
		Size: 1.3 MB (1260570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dae84293a5e75bd15077274b31b14eaec6c0fc94e035b36febae220198d1f2`  
		Last Modified: Tue, 21 Oct 2025 19:27:15 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a9c55bf6a0924e65b32510d0961685bdd8d8f2b10c2db7dd7c96bdd51bf6a9`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 838.6 KB (838585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6208bc17bacacf9b675576e3a0f1ea6703a538aa99a36a8afc4f265ad6606fd4`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e145e2590cb18e81ffe8ac9d21e865b79a70aae4f5cf913d72227d6b5a0c89f`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5e151584a8a323c8c95a64b09e39e356af36f4eaafda1e33ccbd47f82ccb9c`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 11.1 MB (11094690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea721408dbea49d2025fa1a9c571d38cb1fc8f275fc6505f5dad38b4f7f0f44`  
		Last Modified: Mon, 03 Nov 2025 23:16:00 GMT  
		Size: 125.5 MB (125517109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df139f51032436062d10fd724eba3c899f0f3c8bdb77226d7140ecfcc55e6308`  
		Last Modified: Mon, 03 Nov 2025 23:15:47 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:d3def10dd533d48e2cbbf4453012f2197ed4d09a6cfb48880f830a1436e526e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e2fa9bacdd7216a338861d1c288ae6ee8a60f4fc28c1105ec3906ebeb554a2`

```dockerfile
```

-	Layers:
	-	`sha256:32d63c33bb3db7b0d81adf8e25e21c55071e4fe60e7e4a74d6191983d7d6b88b`  
		Last Modified: Tue, 04 Nov 2025 01:45:29 GMT  
		Size: 3.3 MB (3330211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abbb7369c2dac9f8713988834f81b90112f90d7083f3f254112a5711ac640346`  
		Last Modified: Tue, 04 Nov 2025 01:45:30 GMT  
		Size: 28.5 KB (28483 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-bookworm`

```console
$ docker pull ghost@sha256:337ce3180f977caa1a6c0fcd725395994cd580f622bfad1b2e2062cf7642a5cc
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

### `ghost:5-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:f85733f3cbc898d36de4088f2fda14a125f8a49532ec00c7434cb8ea0e421f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb803bfa37a1461f5c31b8082c18f7b30fb4cafa2d430641d448228a6d4e34ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:34:32 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:34:32 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:32 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:34:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:43 GMT
CMD ["node"]
# Tue, 04 Nov 2025 04:33:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 04:33:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 04:33:50 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 04:33:50 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 04:34:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 04:35:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 04:35:07 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 04:35:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 04:35:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:35:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:35:07 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 04:35:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f707883943caee6170d1c96b0e24f29b11404bd9817e8e658e8c24898f94807`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9be599d8cff95c94bc0036ba643b354bfb691616e6f582ee79e08a20071764e`  
		Last Modified: Tue, 04 Nov 2025 00:35:04 GMT  
		Size: 41.0 MB (40977842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561299ddc92fb2324b06da8e6e176820a7eba31727bb4bc1cb1a28403ff4db12`  
		Last Modified: Tue, 04 Nov 2025 00:35:02 GMT  
		Size: 1.7 MB (1712619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7eb6b5a2b17e46a979515b9e341cce1eafc9b6035d440d435715fbb77690bb`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864aed93e665e6fa26d34620ea863882b848dc24e86f0fe197cdced4114e4562`  
		Last Modified: Tue, 04 Nov 2025 04:35:47 GMT  
		Size: 1.2 MB (1247537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba6c8fd4f450c1f7457c81998f7dd13f3010e3a4113093b112b454a1e2d09a4`  
		Last Modified: Tue, 04 Nov 2025 04:35:48 GMT  
		Size: 11.1 MB (11094147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3d3dff4aaa867d1ae255c80633027f39d66e5281984beb46805075f78e11a5`  
		Last Modified: Tue, 04 Nov 2025 04:35:54 GMT  
		Size: 118.0 MB (118018049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d29e5f38b1e0fa7e0f98cae6416943814b9a57577170b459e4451f1db9f44d`  
		Last Modified: Tue, 04 Nov 2025 04:35:47 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:f4217b269e6c02f3b0044770a218ece6b4f9e62e2f2343af1989d7fb9fa0927f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f37142f2048af11deff44531397262046cfa9a752576896fac6401fdc4892e`

```dockerfile
```

-	Layers:
	-	`sha256:8c0305204fbc4eb1195f4a4532034b13bf62f90401195df4f47e23ef7aaf052c`  
		Last Modified: Tue, 04 Nov 2025 10:45:27 GMT  
		Size: 5.5 MB (5543181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4631011bb1a1306639afdeeb7e8acfe2dfbec54142e99360f5adcc478982daa3`  
		Last Modified: Tue, 04 Nov 2025 10:45:28 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:d54af2f62dbe59d10c76ec8b4c87eda9ba3e2a80e130a1270eaa7fd4b094048f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195612293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e008e162f1176295a864de55fd1777a3adbff9626cc579c97fbcce62b8501f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:46:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:47:03 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:47:03 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:47:03 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:47:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:47:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:47:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:47:15 GMT
CMD ["node"]
# Tue, 04 Nov 2025 02:43:46 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 02:43:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 02:43:46 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 02:43:46 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 02:44:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 02:46:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 02:46:49 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 02:46:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 02:46:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:46:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:46:49 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 02:46:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93c37c1fd1b7f4d09c483f03a2a845c305e3e3ecc99b3b52d68d46608ebb3f`  
		Last Modified: Tue, 04 Nov 2025 00:47:34 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7f2cf1babca77eeed4ac645ee2ed904d57e7ee6a13ff624054af478867074d`  
		Last Modified: Tue, 04 Nov 2025 00:47:38 GMT  
		Size: 37.1 MB (37064306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488f9e73958b5133b77535cce142f45578b4297a9b3554e3f83c569f3363b2f`  
		Last Modified: Tue, 04 Nov 2025 00:47:34 GMT  
		Size: 1.7 MB (1712823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb0f6234b40d280dd577f5ff6c58d1b026b669fdb3e89d6e96f2d5a1efcca7f`  
		Last Modified: Tue, 04 Nov 2025 00:47:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e8191b4d8b62dbbdb3ef3d4a6b899a6fede17cb071db5d2bbd145f29b88bd0`  
		Last Modified: Tue, 04 Nov 2025 02:47:32 GMT  
		Size: 1.2 MB (1214355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3102d25ad11605635394177f33ad305073fc8c0267601aadc4a9cbd9a68212`  
		Last Modified: Tue, 04 Nov 2025 02:47:33 GMT  
		Size: 11.1 MB (11094829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deeef39e9f4c1c4d9cf2263beb1ed290d522127aab93d27721ff9806f0a2fe5a`  
		Last Modified: Tue, 04 Nov 2025 02:47:44 GMT  
		Size: 120.6 MB (120587524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d66cc2862765c4676c6164d0f4ed12303ff5421ad0d8be8f792f1cd1b87ae7`  
		Last Modified: Tue, 04 Nov 2025 02:47:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:940a9180000c1e68107a92ebdcfabeb0f181107cd9aa1df4cca5e768eb4ae1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d3cecb5fb064dc47a02da45dbfa06e6ec6cc4d8adb55e0694a81189ff25588`

```dockerfile
```

-	Layers:
	-	`sha256:d03259ddf9f5bea23fc228da9cad31e09474df6b009d025a60263281d9e6e3fa`  
		Last Modified: Tue, 04 Nov 2025 10:45:32 GMT  
		Size: 5.5 MB (5545960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bef53d686d15b6e964d4fa9cf4d4cea8735c5702804503b0776dc18ab6bfd45`  
		Last Modified: Tue, 04 Nov 2025 10:45:33 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b84f862c680ac2c30d07bc0b6c7ebdce04d4a85e0fd7045807073e95cc3a88e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201178174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3c609ac0e52a737db94f0a2a90d598558a4f2a5fd52f4c64ff045464a9d384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:23 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:35:42 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:35:42 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:42 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:35:53 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:35:53 GMT
CMD ["node"]
# Tue, 04 Nov 2025 01:48:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 01:48:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 01:48:51 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 01:48:51 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 01:49:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 01:50:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 01:50:19 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 01:50:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 01:50:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:50:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:50:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 01:50:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e3e431f7a520df14961d4498593d85568abcee7af80df09bfb1ecaef7cd45`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd1f8ab98ef1e2152eab9b695ec2f87db4d02435d64fdec15bd10a153ff849`  
		Last Modified: Tue, 04 Nov 2025 00:36:20 GMT  
		Size: 40.9 MB (40939662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaa03f4a05ff40bcfbe40175a2dbd854534498b254584994ed85d776bb55587`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 1.7 MB (1712633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6570b58c3e47b958ae4b68f789413ade8fe66580a20c717b3cb1e69f0c133ebf`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663ae620ac190c68e5d83a83b3d33b0eb2eb423a03fac16114cd3cd12cc5019f`  
		Last Modified: Tue, 04 Nov 2025 01:51:03 GMT  
		Size: 1.2 MB (1201430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9c0870ca41dfc91a0e2a298cdc47e8114d6f3d09c14d764b2d753f5f0670ce`  
		Last Modified: Tue, 04 Nov 2025 01:51:03 GMT  
		Size: 11.1 MB (11094919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602531b4420813b49243982ad8a1c2a9549dbae632743b32cb5a9805b2403887`  
		Last Modified: Tue, 04 Nov 2025 01:51:18 GMT  
		Size: 118.1 MB (118122828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295d0e4df7a9fe45640c39d05aa3a0c0eaaf7a3087e6211d12a3e53d0e9b6312`  
		Last Modified: Tue, 04 Nov 2025 01:51:02 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:445ef3bc796bab18ada3fba661be331b721a771a43efdc88647eb5d116d4c68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5569425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4965280d091d4279629434307cdbaf3fb262b9134a9a4d73aab1897800946f`

```dockerfile
```

-	Layers:
	-	`sha256:067f8b997a5e51ef10a4601a130dfc95344c8ee4b8b4a912a5304279072e0562`  
		Last Modified: Tue, 04 Nov 2025 10:45:37 GMT  
		Size: 5.5 MB (5543508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:321b4338d423ea63134b074ba90c5d4d27bc35d8d7a43c0b0c1ddcc801008c85`  
		Last Modified: Tue, 04 Nov 2025 10:45:38 GMT  
		Size: 25.9 KB (25917 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:fedc92789cc63ec80586657b88fa4c694f5ef240cd4f4a2b6c1688440c7a4439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204802905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c301e77ea9647ac3183392844f94ef4ebc65b70ae40551ea9eadc7d1b9625a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:33:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 03:37:01 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 03:37:01 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:37:01 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 03:37:10 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:37:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:37:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:37:10 GMT
CMD ["node"]
# Tue, 04 Nov 2025 13:34:35 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 13:34:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 13:34:35 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 13:34:35 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 13:34:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 13:37:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 13:37:13 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 13:37:13 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 13:37:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 13:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 13:37:13 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 13:37:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b483b0df66cd8c70ba210c61fdc3840348da24bad86177f3799a15a254e527`  
		Last Modified: Tue, 04 Nov 2025 03:34:01 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a391e545ed0d8aeddbbfdf6c58840bd79044b2d7724a7f9e2f4b25f94cd446`  
		Last Modified: Tue, 04 Nov 2025 03:37:41 GMT  
		Size: 41.2 MB (41222577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff94fd9f029756b1291b5b34bfc358a41e9c02a77d415cf91c92e6480c8cc12`  
		Last Modified: Tue, 04 Nov 2025 03:37:39 GMT  
		Size: 1.7 MB (1712621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb828a655db1ab796ec4ec301dbddaed50020b282af492e0ad200dcd1a7f9a7`  
		Last Modified: Tue, 04 Nov 2025 03:37:39 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f328b3f0fc2f5ec6a0ce9d45ffce274cdc93a98a55cd8eaaa4d1cb295fb11a`  
		Last Modified: Tue, 04 Nov 2025 13:38:12 GMT  
		Size: 1.2 MB (1221301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84250905d6e664f6e19a3907889c1832e155c4a9e639f732621d0ad78b5eea0f`  
		Last Modified: Tue, 04 Nov 2025 13:38:15 GMT  
		Size: 11.1 MB (11093207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaf51cd926003ef4b173028a768cbd8235b7fab10f8364c526e52155d74609b`  
		Last Modified: Tue, 04 Nov 2025 13:38:22 GMT  
		Size: 122.7 MB (122664325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002ebcdf1e703e7b6e8e6dedf4cff0aba49d24404fce1007cd77b34af1011f7c`  
		Last Modified: Tue, 04 Nov 2025 13:38:12 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:aea28f5f061e7e1fe6c72475dc569a1ff0dcf919d99e365cb48cd601995c2908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7f4f9dbf6f2371841cfe530c36b8341ca0772822038bd3983ca67428f477bf`

```dockerfile
```

-	Layers:
	-	`sha256:7964a06228d679e34749309df911e4f993cfdb332d28c9b0117e17e9a52c4197`  
		Last Modified: Tue, 04 Nov 2025 16:45:31 GMT  
		Size: 5.5 MB (5537004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9aa56bb8d72e1ec060d747be18da6e100963612bda5035ca87306b345192c5d`  
		Last Modified: Tue, 04 Nov 2025 16:45:32 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130`

```console
$ docker pull ghost@sha256:337ce3180f977caa1a6c0fcd725395994cd580f622bfad1b2e2062cf7642a5cc
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

### `ghost:5.130` - linux; amd64

```console
$ docker pull ghost@sha256:f85733f3cbc898d36de4088f2fda14a125f8a49532ec00c7434cb8ea0e421f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb803bfa37a1461f5c31b8082c18f7b30fb4cafa2d430641d448228a6d4e34ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:34:32 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:34:32 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:32 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:34:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:43 GMT
CMD ["node"]
# Tue, 04 Nov 2025 04:33:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 04:33:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 04:33:50 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 04:33:50 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 04:34:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 04:35:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 04:35:07 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 04:35:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 04:35:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:35:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:35:07 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 04:35:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f707883943caee6170d1c96b0e24f29b11404bd9817e8e658e8c24898f94807`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9be599d8cff95c94bc0036ba643b354bfb691616e6f582ee79e08a20071764e`  
		Last Modified: Tue, 04 Nov 2025 00:35:04 GMT  
		Size: 41.0 MB (40977842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561299ddc92fb2324b06da8e6e176820a7eba31727bb4bc1cb1a28403ff4db12`  
		Last Modified: Tue, 04 Nov 2025 00:35:02 GMT  
		Size: 1.7 MB (1712619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7eb6b5a2b17e46a979515b9e341cce1eafc9b6035d440d435715fbb77690bb`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864aed93e665e6fa26d34620ea863882b848dc24e86f0fe197cdced4114e4562`  
		Last Modified: Tue, 04 Nov 2025 04:35:47 GMT  
		Size: 1.2 MB (1247537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba6c8fd4f450c1f7457c81998f7dd13f3010e3a4113093b112b454a1e2d09a4`  
		Last Modified: Tue, 04 Nov 2025 04:35:48 GMT  
		Size: 11.1 MB (11094147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3d3dff4aaa867d1ae255c80633027f39d66e5281984beb46805075f78e11a5`  
		Last Modified: Tue, 04 Nov 2025 04:35:54 GMT  
		Size: 118.0 MB (118018049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d29e5f38b1e0fa7e0f98cae6416943814b9a57577170b459e4451f1db9f44d`  
		Last Modified: Tue, 04 Nov 2025 04:35:47 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:f4217b269e6c02f3b0044770a218ece6b4f9e62e2f2343af1989d7fb9fa0927f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f37142f2048af11deff44531397262046cfa9a752576896fac6401fdc4892e`

```dockerfile
```

-	Layers:
	-	`sha256:8c0305204fbc4eb1195f4a4532034b13bf62f90401195df4f47e23ef7aaf052c`  
		Last Modified: Tue, 04 Nov 2025 10:45:27 GMT  
		Size: 5.5 MB (5543181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4631011bb1a1306639afdeeb7e8acfe2dfbec54142e99360f5adcc478982daa3`  
		Last Modified: Tue, 04 Nov 2025 10:45:28 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; arm variant v7

```console
$ docker pull ghost@sha256:d54af2f62dbe59d10c76ec8b4c87eda9ba3e2a80e130a1270eaa7fd4b094048f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195612293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e008e162f1176295a864de55fd1777a3adbff9626cc579c97fbcce62b8501f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:46:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:47:03 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:47:03 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:47:03 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:47:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:47:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:47:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:47:15 GMT
CMD ["node"]
# Tue, 04 Nov 2025 02:43:46 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 02:43:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 02:43:46 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 02:43:46 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 02:44:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 02:46:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 02:46:49 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 02:46:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 02:46:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:46:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:46:49 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 02:46:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93c37c1fd1b7f4d09c483f03a2a845c305e3e3ecc99b3b52d68d46608ebb3f`  
		Last Modified: Tue, 04 Nov 2025 00:47:34 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7f2cf1babca77eeed4ac645ee2ed904d57e7ee6a13ff624054af478867074d`  
		Last Modified: Tue, 04 Nov 2025 00:47:38 GMT  
		Size: 37.1 MB (37064306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488f9e73958b5133b77535cce142f45578b4297a9b3554e3f83c569f3363b2f`  
		Last Modified: Tue, 04 Nov 2025 00:47:34 GMT  
		Size: 1.7 MB (1712823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb0f6234b40d280dd577f5ff6c58d1b026b669fdb3e89d6e96f2d5a1efcca7f`  
		Last Modified: Tue, 04 Nov 2025 00:47:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e8191b4d8b62dbbdb3ef3d4a6b899a6fede17cb071db5d2bbd145f29b88bd0`  
		Last Modified: Tue, 04 Nov 2025 02:47:32 GMT  
		Size: 1.2 MB (1214355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3102d25ad11605635394177f33ad305073fc8c0267601aadc4a9cbd9a68212`  
		Last Modified: Tue, 04 Nov 2025 02:47:33 GMT  
		Size: 11.1 MB (11094829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deeef39e9f4c1c4d9cf2263beb1ed290d522127aab93d27721ff9806f0a2fe5a`  
		Last Modified: Tue, 04 Nov 2025 02:47:44 GMT  
		Size: 120.6 MB (120587524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d66cc2862765c4676c6164d0f4ed12303ff5421ad0d8be8f792f1cd1b87ae7`  
		Last Modified: Tue, 04 Nov 2025 02:47:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:940a9180000c1e68107a92ebdcfabeb0f181107cd9aa1df4cca5e768eb4ae1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d3cecb5fb064dc47a02da45dbfa06e6ec6cc4d8adb55e0694a81189ff25588`

```dockerfile
```

-	Layers:
	-	`sha256:d03259ddf9f5bea23fc228da9cad31e09474df6b009d025a60263281d9e6e3fa`  
		Last Modified: Tue, 04 Nov 2025 10:45:32 GMT  
		Size: 5.5 MB (5545960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bef53d686d15b6e964d4fa9cf4d4cea8735c5702804503b0776dc18ab6bfd45`  
		Last Modified: Tue, 04 Nov 2025 10:45:33 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b84f862c680ac2c30d07bc0b6c7ebdce04d4a85e0fd7045807073e95cc3a88e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201178174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3c609ac0e52a737db94f0a2a90d598558a4f2a5fd52f4c64ff045464a9d384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:23 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:35:42 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:35:42 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:42 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:35:53 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:35:53 GMT
CMD ["node"]
# Tue, 04 Nov 2025 01:48:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 01:48:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 01:48:51 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 01:48:51 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 01:49:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 01:50:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 01:50:19 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 01:50:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 01:50:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:50:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:50:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 01:50:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e3e431f7a520df14961d4498593d85568abcee7af80df09bfb1ecaef7cd45`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd1f8ab98ef1e2152eab9b695ec2f87db4d02435d64fdec15bd10a153ff849`  
		Last Modified: Tue, 04 Nov 2025 00:36:20 GMT  
		Size: 40.9 MB (40939662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaa03f4a05ff40bcfbe40175a2dbd854534498b254584994ed85d776bb55587`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 1.7 MB (1712633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6570b58c3e47b958ae4b68f789413ade8fe66580a20c717b3cb1e69f0c133ebf`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663ae620ac190c68e5d83a83b3d33b0eb2eb423a03fac16114cd3cd12cc5019f`  
		Last Modified: Tue, 04 Nov 2025 01:51:03 GMT  
		Size: 1.2 MB (1201430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9c0870ca41dfc91a0e2a298cdc47e8114d6f3d09c14d764b2d753f5f0670ce`  
		Last Modified: Tue, 04 Nov 2025 01:51:03 GMT  
		Size: 11.1 MB (11094919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602531b4420813b49243982ad8a1c2a9549dbae632743b32cb5a9805b2403887`  
		Last Modified: Tue, 04 Nov 2025 01:51:18 GMT  
		Size: 118.1 MB (118122828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295d0e4df7a9fe45640c39d05aa3a0c0eaaf7a3087e6211d12a3e53d0e9b6312`  
		Last Modified: Tue, 04 Nov 2025 01:51:02 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:445ef3bc796bab18ada3fba661be331b721a771a43efdc88647eb5d116d4c68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5569425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4965280d091d4279629434307cdbaf3fb262b9134a9a4d73aab1897800946f`

```dockerfile
```

-	Layers:
	-	`sha256:067f8b997a5e51ef10a4601a130dfc95344c8ee4b8b4a912a5304279072e0562`  
		Last Modified: Tue, 04 Nov 2025 10:45:37 GMT  
		Size: 5.5 MB (5543508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:321b4338d423ea63134b074ba90c5d4d27bc35d8d7a43c0b0c1ddcc801008c85`  
		Last Modified: Tue, 04 Nov 2025 10:45:38 GMT  
		Size: 25.9 KB (25917 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; s390x

```console
$ docker pull ghost@sha256:fedc92789cc63ec80586657b88fa4c694f5ef240cd4f4a2b6c1688440c7a4439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204802905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c301e77ea9647ac3183392844f94ef4ebc65b70ae40551ea9eadc7d1b9625a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:33:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 03:37:01 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 03:37:01 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:37:01 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 03:37:10 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:37:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:37:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:37:10 GMT
CMD ["node"]
# Tue, 04 Nov 2025 13:34:35 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 13:34:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 13:34:35 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 13:34:35 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 13:34:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 13:37:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 13:37:13 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 13:37:13 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 13:37:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 13:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 13:37:13 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 13:37:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b483b0df66cd8c70ba210c61fdc3840348da24bad86177f3799a15a254e527`  
		Last Modified: Tue, 04 Nov 2025 03:34:01 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a391e545ed0d8aeddbbfdf6c58840bd79044b2d7724a7f9e2f4b25f94cd446`  
		Last Modified: Tue, 04 Nov 2025 03:37:41 GMT  
		Size: 41.2 MB (41222577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff94fd9f029756b1291b5b34bfc358a41e9c02a77d415cf91c92e6480c8cc12`  
		Last Modified: Tue, 04 Nov 2025 03:37:39 GMT  
		Size: 1.7 MB (1712621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb828a655db1ab796ec4ec301dbddaed50020b282af492e0ad200dcd1a7f9a7`  
		Last Modified: Tue, 04 Nov 2025 03:37:39 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f328b3f0fc2f5ec6a0ce9d45ffce274cdc93a98a55cd8eaaa4d1cb295fb11a`  
		Last Modified: Tue, 04 Nov 2025 13:38:12 GMT  
		Size: 1.2 MB (1221301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84250905d6e664f6e19a3907889c1832e155c4a9e639f732621d0ad78b5eea0f`  
		Last Modified: Tue, 04 Nov 2025 13:38:15 GMT  
		Size: 11.1 MB (11093207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaf51cd926003ef4b173028a768cbd8235b7fab10f8364c526e52155d74609b`  
		Last Modified: Tue, 04 Nov 2025 13:38:22 GMT  
		Size: 122.7 MB (122664325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002ebcdf1e703e7b6e8e6dedf4cff0aba49d24404fce1007cd77b34af1011f7c`  
		Last Modified: Tue, 04 Nov 2025 13:38:12 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:aea28f5f061e7e1fe6c72475dc569a1ff0dcf919d99e365cb48cd601995c2908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7f4f9dbf6f2371841cfe530c36b8341ca0772822038bd3983ca67428f477bf`

```dockerfile
```

-	Layers:
	-	`sha256:7964a06228d679e34749309df911e4f993cfdb332d28c9b0117e17e9a52c4197`  
		Last Modified: Tue, 04 Nov 2025 16:45:31 GMT  
		Size: 5.5 MB (5537004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9aa56bb8d72e1ec060d747be18da6e100963612bda5035ca87306b345192c5d`  
		Last Modified: Tue, 04 Nov 2025 16:45:32 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130-alpine`

```console
$ docker pull ghost@sha256:6cca0c2a8a2ca5f57e31bf311e8c35b570be0b0c2451c9c37bea55197bdfeb68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:0f70a24b1ba6a1d3997eaf4853a6e6f6d6fafb0446c28f3deeaf3a01252423f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175511698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68920e05396cd4669b7e3c46d22a38fb4333b55009f4ea79fa4b6209db38440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:24 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:14:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:14:26 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:14:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:14:26 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:14:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e45a9660cfaebbbac9bba98180aa28b3966b7f2462d132c46f51a1f5b25a64`  
		Last Modified: Tue, 21 Oct 2025 20:19:28 GMT  
		Size: 42.8 MB (42750841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74e4ed823e9560b3fe51c0cab47dbfdfc4b12453604319408ec58708fb9e720`  
		Last Modified: Tue, 21 Oct 2025 20:19:17 GMT  
		Size: 1.3 MB (1260590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04d522c98fe12816b2bcddf8413fca73645f8fa60f287c672f58bcc7f0fa38`  
		Last Modified: Tue, 21 Oct 2025 20:19:16 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0f9a897060feb550287b8d83fcf4ee55da3c30f54db1edf978b006db787df`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 777.0 KB (777045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b382b367f507fc850a39a16fec12749f6c1306dc08e0e4f5d9fb4e9fb87140`  
		Last Modified: Mon, 03 Nov 2025 23:15:08 GMT  
		Size: 923.4 KB (923439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4892805e65559d25032860f128b6ffde24688439b15eafae4582e7433248835`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be658ce9c8e59f7aa9d714b669e868cc97bb892900145e917445a00f7684af`  
		Last Modified: Mon, 03 Nov 2025 23:15:09 GMT  
		Size: 11.1 MB (11093048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67e9dd34d742b7cb05cf61410a70c7992f27db78d903721c0c4cb0550b4883`  
		Last Modified: Mon, 03 Nov 2025 23:15:17 GMT  
		Size: 114.9 MB (114903085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa3dd720a5026dbd84f0306d99be03e7e0f6481b674c2a664c60743d5b0bf5`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:0705a01a45b41466c233e6ff85abb3245f22f31baa322462468a6c9d259c7ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5c4812ee7cd0ae829317bd459870791c1165f3b1ece1398199ae4792524700`

```dockerfile
```

-	Layers:
	-	`sha256:1210e51ac71ad4e5f3362abb7b760cf9634edaa2629be743b66e7e65cc2bf36d`  
		Last Modified: Tue, 04 Nov 2025 01:45:24 GMT  
		Size: 3.3 MB (3330079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e4429e809841d6839249a064f9f674748ca2445fab5bbf04eeabf3c5053ace`  
		Last Modified: Tue, 04 Nov 2025 01:45:25 GMT  
		Size: 28.3 KB (28295 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:86bf1443622143bb16bee447fe4c778ad3e965699ee809c01355752173c0923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186152453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3311524bf8d21f721e8381834f51617e7085c55d1156e168336a952037c0819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:41 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:15:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:15:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:15:00 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:15:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae67534e7d0aa8a27cfb7e3ecb9727f2ce2a6dd5b721d5392c27b91fc68b7f13`  
		Last Modified: Tue, 21 Oct 2025 19:27:20 GMT  
		Size: 42.4 MB (42425867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf56a7feaf43fe338cd74317fda62608ec88dfd616dd5bff62f6f11b631692`  
		Last Modified: Tue, 21 Oct 2025 19:27:16 GMT  
		Size: 1.3 MB (1260570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dae84293a5e75bd15077274b31b14eaec6c0fc94e035b36febae220198d1f2`  
		Last Modified: Tue, 21 Oct 2025 19:27:15 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a9c55bf6a0924e65b32510d0961685bdd8d8f2b10c2db7dd7c96bdd51bf6a9`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 838.6 KB (838585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6208bc17bacacf9b675576e3a0f1ea6703a538aa99a36a8afc4f265ad6606fd4`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e145e2590cb18e81ffe8ac9d21e865b79a70aae4f5cf913d72227d6b5a0c89f`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5e151584a8a323c8c95a64b09e39e356af36f4eaafda1e33ccbd47f82ccb9c`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 11.1 MB (11094690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea721408dbea49d2025fa1a9c571d38cb1fc8f275fc6505f5dad38b4f7f0f44`  
		Last Modified: Mon, 03 Nov 2025 23:16:00 GMT  
		Size: 125.5 MB (125517109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df139f51032436062d10fd724eba3c899f0f3c8bdb77226d7140ecfcc55e6308`  
		Last Modified: Mon, 03 Nov 2025 23:15:47 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:d3def10dd533d48e2cbbf4453012f2197ed4d09a6cfb48880f830a1436e526e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e2fa9bacdd7216a338861d1c288ae6ee8a60f4fc28c1105ec3906ebeb554a2`

```dockerfile
```

-	Layers:
	-	`sha256:32d63c33bb3db7b0d81adf8e25e21c55071e4fe60e7e4a74d6191983d7d6b88b`  
		Last Modified: Tue, 04 Nov 2025 01:45:29 GMT  
		Size: 3.3 MB (3330211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abbb7369c2dac9f8713988834f81b90112f90d7083f3f254112a5711ac640346`  
		Last Modified: Tue, 04 Nov 2025 01:45:30 GMT  
		Size: 28.5 KB (28483 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130-alpine3.22`

```console
$ docker pull ghost@sha256:6cca0c2a8a2ca5f57e31bf311e8c35b570be0b0c2451c9c37bea55197bdfeb68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130-alpine3.22` - linux; amd64

```console
$ docker pull ghost@sha256:0f70a24b1ba6a1d3997eaf4853a6e6f6d6fafb0446c28f3deeaf3a01252423f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175511698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68920e05396cd4669b7e3c46d22a38fb4333b55009f4ea79fa4b6209db38440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:24 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:14:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:14:26 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:14:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:14:26 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:14:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e45a9660cfaebbbac9bba98180aa28b3966b7f2462d132c46f51a1f5b25a64`  
		Last Modified: Tue, 21 Oct 2025 20:19:28 GMT  
		Size: 42.8 MB (42750841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74e4ed823e9560b3fe51c0cab47dbfdfc4b12453604319408ec58708fb9e720`  
		Last Modified: Tue, 21 Oct 2025 20:19:17 GMT  
		Size: 1.3 MB (1260590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04d522c98fe12816b2bcddf8413fca73645f8fa60f287c672f58bcc7f0fa38`  
		Last Modified: Tue, 21 Oct 2025 20:19:16 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0f9a897060feb550287b8d83fcf4ee55da3c30f54db1edf978b006db787df`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 777.0 KB (777045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b382b367f507fc850a39a16fec12749f6c1306dc08e0e4f5d9fb4e9fb87140`  
		Last Modified: Mon, 03 Nov 2025 23:15:08 GMT  
		Size: 923.4 KB (923439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4892805e65559d25032860f128b6ffde24688439b15eafae4582e7433248835`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be658ce9c8e59f7aa9d714b669e868cc97bb892900145e917445a00f7684af`  
		Last Modified: Mon, 03 Nov 2025 23:15:09 GMT  
		Size: 11.1 MB (11093048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67e9dd34d742b7cb05cf61410a70c7992f27db78d903721c0c4cb0550b4883`  
		Last Modified: Mon, 03 Nov 2025 23:15:17 GMT  
		Size: 114.9 MB (114903085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa3dd720a5026dbd84f0306d99be03e7e0f6481b674c2a664c60743d5b0bf5`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:0705a01a45b41466c233e6ff85abb3245f22f31baa322462468a6c9d259c7ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5c4812ee7cd0ae829317bd459870791c1165f3b1ece1398199ae4792524700`

```dockerfile
```

-	Layers:
	-	`sha256:1210e51ac71ad4e5f3362abb7b760cf9634edaa2629be743b66e7e65cc2bf36d`  
		Last Modified: Tue, 04 Nov 2025 01:45:24 GMT  
		Size: 3.3 MB (3330079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e4429e809841d6839249a064f9f674748ca2445fab5bbf04eeabf3c5053ace`  
		Last Modified: Tue, 04 Nov 2025 01:45:25 GMT  
		Size: 28.3 KB (28295 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:86bf1443622143bb16bee447fe4c778ad3e965699ee809c01355752173c0923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186152453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3311524bf8d21f721e8381834f51617e7085c55d1156e168336a952037c0819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:41 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:15:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:15:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:15:00 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:15:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae67534e7d0aa8a27cfb7e3ecb9727f2ce2a6dd5b721d5392c27b91fc68b7f13`  
		Last Modified: Tue, 21 Oct 2025 19:27:20 GMT  
		Size: 42.4 MB (42425867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf56a7feaf43fe338cd74317fda62608ec88dfd616dd5bff62f6f11b631692`  
		Last Modified: Tue, 21 Oct 2025 19:27:16 GMT  
		Size: 1.3 MB (1260570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dae84293a5e75bd15077274b31b14eaec6c0fc94e035b36febae220198d1f2`  
		Last Modified: Tue, 21 Oct 2025 19:27:15 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a9c55bf6a0924e65b32510d0961685bdd8d8f2b10c2db7dd7c96bdd51bf6a9`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 838.6 KB (838585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6208bc17bacacf9b675576e3a0f1ea6703a538aa99a36a8afc4f265ad6606fd4`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e145e2590cb18e81ffe8ac9d21e865b79a70aae4f5cf913d72227d6b5a0c89f`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5e151584a8a323c8c95a64b09e39e356af36f4eaafda1e33ccbd47f82ccb9c`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 11.1 MB (11094690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea721408dbea49d2025fa1a9c571d38cb1fc8f275fc6505f5dad38b4f7f0f44`  
		Last Modified: Mon, 03 Nov 2025 23:16:00 GMT  
		Size: 125.5 MB (125517109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df139f51032436062d10fd724eba3c899f0f3c8bdb77226d7140ecfcc55e6308`  
		Last Modified: Mon, 03 Nov 2025 23:15:47 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:d3def10dd533d48e2cbbf4453012f2197ed4d09a6cfb48880f830a1436e526e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e2fa9bacdd7216a338861d1c288ae6ee8a60f4fc28c1105ec3906ebeb554a2`

```dockerfile
```

-	Layers:
	-	`sha256:32d63c33bb3db7b0d81adf8e25e21c55071e4fe60e7e4a74d6191983d7d6b88b`  
		Last Modified: Tue, 04 Nov 2025 01:45:29 GMT  
		Size: 3.3 MB (3330211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abbb7369c2dac9f8713988834f81b90112f90d7083f3f254112a5711ac640346`  
		Last Modified: Tue, 04 Nov 2025 01:45:30 GMT  
		Size: 28.5 KB (28483 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130-bookworm`

```console
$ docker pull ghost@sha256:337ce3180f977caa1a6c0fcd725395994cd580f622bfad1b2e2062cf7642a5cc
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

### `ghost:5.130-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:f85733f3cbc898d36de4088f2fda14a125f8a49532ec00c7434cb8ea0e421f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb803bfa37a1461f5c31b8082c18f7b30fb4cafa2d430641d448228a6d4e34ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:34:32 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:34:32 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:32 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:34:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:43 GMT
CMD ["node"]
# Tue, 04 Nov 2025 04:33:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 04:33:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 04:33:50 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 04:33:50 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 04:34:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 04:35:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 04:35:07 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 04:35:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 04:35:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:35:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:35:07 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 04:35:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f707883943caee6170d1c96b0e24f29b11404bd9817e8e658e8c24898f94807`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9be599d8cff95c94bc0036ba643b354bfb691616e6f582ee79e08a20071764e`  
		Last Modified: Tue, 04 Nov 2025 00:35:04 GMT  
		Size: 41.0 MB (40977842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561299ddc92fb2324b06da8e6e176820a7eba31727bb4bc1cb1a28403ff4db12`  
		Last Modified: Tue, 04 Nov 2025 00:35:02 GMT  
		Size: 1.7 MB (1712619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7eb6b5a2b17e46a979515b9e341cce1eafc9b6035d440d435715fbb77690bb`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864aed93e665e6fa26d34620ea863882b848dc24e86f0fe197cdced4114e4562`  
		Last Modified: Tue, 04 Nov 2025 04:35:47 GMT  
		Size: 1.2 MB (1247537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba6c8fd4f450c1f7457c81998f7dd13f3010e3a4113093b112b454a1e2d09a4`  
		Last Modified: Tue, 04 Nov 2025 04:35:48 GMT  
		Size: 11.1 MB (11094147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3d3dff4aaa867d1ae255c80633027f39d66e5281984beb46805075f78e11a5`  
		Last Modified: Tue, 04 Nov 2025 04:35:54 GMT  
		Size: 118.0 MB (118018049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d29e5f38b1e0fa7e0f98cae6416943814b9a57577170b459e4451f1db9f44d`  
		Last Modified: Tue, 04 Nov 2025 04:35:47 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:f4217b269e6c02f3b0044770a218ece6b4f9e62e2f2343af1989d7fb9fa0927f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f37142f2048af11deff44531397262046cfa9a752576896fac6401fdc4892e`

```dockerfile
```

-	Layers:
	-	`sha256:8c0305204fbc4eb1195f4a4532034b13bf62f90401195df4f47e23ef7aaf052c`  
		Last Modified: Tue, 04 Nov 2025 10:45:27 GMT  
		Size: 5.5 MB (5543181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4631011bb1a1306639afdeeb7e8acfe2dfbec54142e99360f5adcc478982daa3`  
		Last Modified: Tue, 04 Nov 2025 10:45:28 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:d54af2f62dbe59d10c76ec8b4c87eda9ba3e2a80e130a1270eaa7fd4b094048f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195612293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e008e162f1176295a864de55fd1777a3adbff9626cc579c97fbcce62b8501f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:46:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:47:03 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:47:03 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:47:03 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:47:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:47:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:47:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:47:15 GMT
CMD ["node"]
# Tue, 04 Nov 2025 02:43:46 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 02:43:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 02:43:46 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 02:43:46 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 02:44:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 02:46:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 02:46:49 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 02:46:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 02:46:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:46:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:46:49 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 02:46:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93c37c1fd1b7f4d09c483f03a2a845c305e3e3ecc99b3b52d68d46608ebb3f`  
		Last Modified: Tue, 04 Nov 2025 00:47:34 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7f2cf1babca77eeed4ac645ee2ed904d57e7ee6a13ff624054af478867074d`  
		Last Modified: Tue, 04 Nov 2025 00:47:38 GMT  
		Size: 37.1 MB (37064306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488f9e73958b5133b77535cce142f45578b4297a9b3554e3f83c569f3363b2f`  
		Last Modified: Tue, 04 Nov 2025 00:47:34 GMT  
		Size: 1.7 MB (1712823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb0f6234b40d280dd577f5ff6c58d1b026b669fdb3e89d6e96f2d5a1efcca7f`  
		Last Modified: Tue, 04 Nov 2025 00:47:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e8191b4d8b62dbbdb3ef3d4a6b899a6fede17cb071db5d2bbd145f29b88bd0`  
		Last Modified: Tue, 04 Nov 2025 02:47:32 GMT  
		Size: 1.2 MB (1214355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3102d25ad11605635394177f33ad305073fc8c0267601aadc4a9cbd9a68212`  
		Last Modified: Tue, 04 Nov 2025 02:47:33 GMT  
		Size: 11.1 MB (11094829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deeef39e9f4c1c4d9cf2263beb1ed290d522127aab93d27721ff9806f0a2fe5a`  
		Last Modified: Tue, 04 Nov 2025 02:47:44 GMT  
		Size: 120.6 MB (120587524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d66cc2862765c4676c6164d0f4ed12303ff5421ad0d8be8f792f1cd1b87ae7`  
		Last Modified: Tue, 04 Nov 2025 02:47:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:940a9180000c1e68107a92ebdcfabeb0f181107cd9aa1df4cca5e768eb4ae1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d3cecb5fb064dc47a02da45dbfa06e6ec6cc4d8adb55e0694a81189ff25588`

```dockerfile
```

-	Layers:
	-	`sha256:d03259ddf9f5bea23fc228da9cad31e09474df6b009d025a60263281d9e6e3fa`  
		Last Modified: Tue, 04 Nov 2025 10:45:32 GMT  
		Size: 5.5 MB (5545960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bef53d686d15b6e964d4fa9cf4d4cea8735c5702804503b0776dc18ab6bfd45`  
		Last Modified: Tue, 04 Nov 2025 10:45:33 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b84f862c680ac2c30d07bc0b6c7ebdce04d4a85e0fd7045807073e95cc3a88e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201178174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3c609ac0e52a737db94f0a2a90d598558a4f2a5fd52f4c64ff045464a9d384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:23 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:35:42 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:35:42 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:42 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:35:53 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:35:53 GMT
CMD ["node"]
# Tue, 04 Nov 2025 01:48:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 01:48:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 01:48:51 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 01:48:51 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 01:49:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 01:50:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 01:50:19 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 01:50:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 01:50:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:50:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:50:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 01:50:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e3e431f7a520df14961d4498593d85568abcee7af80df09bfb1ecaef7cd45`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd1f8ab98ef1e2152eab9b695ec2f87db4d02435d64fdec15bd10a153ff849`  
		Last Modified: Tue, 04 Nov 2025 00:36:20 GMT  
		Size: 40.9 MB (40939662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaa03f4a05ff40bcfbe40175a2dbd854534498b254584994ed85d776bb55587`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 1.7 MB (1712633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6570b58c3e47b958ae4b68f789413ade8fe66580a20c717b3cb1e69f0c133ebf`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663ae620ac190c68e5d83a83b3d33b0eb2eb423a03fac16114cd3cd12cc5019f`  
		Last Modified: Tue, 04 Nov 2025 01:51:03 GMT  
		Size: 1.2 MB (1201430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9c0870ca41dfc91a0e2a298cdc47e8114d6f3d09c14d764b2d753f5f0670ce`  
		Last Modified: Tue, 04 Nov 2025 01:51:03 GMT  
		Size: 11.1 MB (11094919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602531b4420813b49243982ad8a1c2a9549dbae632743b32cb5a9805b2403887`  
		Last Modified: Tue, 04 Nov 2025 01:51:18 GMT  
		Size: 118.1 MB (118122828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295d0e4df7a9fe45640c39d05aa3a0c0eaaf7a3087e6211d12a3e53d0e9b6312`  
		Last Modified: Tue, 04 Nov 2025 01:51:02 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:445ef3bc796bab18ada3fba661be331b721a771a43efdc88647eb5d116d4c68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5569425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4965280d091d4279629434307cdbaf3fb262b9134a9a4d73aab1897800946f`

```dockerfile
```

-	Layers:
	-	`sha256:067f8b997a5e51ef10a4601a130dfc95344c8ee4b8b4a912a5304279072e0562`  
		Last Modified: Tue, 04 Nov 2025 10:45:37 GMT  
		Size: 5.5 MB (5543508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:321b4338d423ea63134b074ba90c5d4d27bc35d8d7a43c0b0c1ddcc801008c85`  
		Last Modified: Tue, 04 Nov 2025 10:45:38 GMT  
		Size: 25.9 KB (25917 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:fedc92789cc63ec80586657b88fa4c694f5ef240cd4f4a2b6c1688440c7a4439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204802905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c301e77ea9647ac3183392844f94ef4ebc65b70ae40551ea9eadc7d1b9625a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:33:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 03:37:01 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 03:37:01 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:37:01 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 03:37:10 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:37:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:37:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:37:10 GMT
CMD ["node"]
# Tue, 04 Nov 2025 13:34:35 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 13:34:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 13:34:35 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 13:34:35 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 13:34:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 13:37:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 13:37:13 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 13:37:13 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 13:37:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 13:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 13:37:13 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 13:37:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b483b0df66cd8c70ba210c61fdc3840348da24bad86177f3799a15a254e527`  
		Last Modified: Tue, 04 Nov 2025 03:34:01 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a391e545ed0d8aeddbbfdf6c58840bd79044b2d7724a7f9e2f4b25f94cd446`  
		Last Modified: Tue, 04 Nov 2025 03:37:41 GMT  
		Size: 41.2 MB (41222577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff94fd9f029756b1291b5b34bfc358a41e9c02a77d415cf91c92e6480c8cc12`  
		Last Modified: Tue, 04 Nov 2025 03:37:39 GMT  
		Size: 1.7 MB (1712621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb828a655db1ab796ec4ec301dbddaed50020b282af492e0ad200dcd1a7f9a7`  
		Last Modified: Tue, 04 Nov 2025 03:37:39 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f328b3f0fc2f5ec6a0ce9d45ffce274cdc93a98a55cd8eaaa4d1cb295fb11a`  
		Last Modified: Tue, 04 Nov 2025 13:38:12 GMT  
		Size: 1.2 MB (1221301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84250905d6e664f6e19a3907889c1832e155c4a9e639f732621d0ad78b5eea0f`  
		Last Modified: Tue, 04 Nov 2025 13:38:15 GMT  
		Size: 11.1 MB (11093207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaf51cd926003ef4b173028a768cbd8235b7fab10f8364c526e52155d74609b`  
		Last Modified: Tue, 04 Nov 2025 13:38:22 GMT  
		Size: 122.7 MB (122664325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002ebcdf1e703e7b6e8e6dedf4cff0aba49d24404fce1007cd77b34af1011f7c`  
		Last Modified: Tue, 04 Nov 2025 13:38:12 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:aea28f5f061e7e1fe6c72475dc569a1ff0dcf919d99e365cb48cd601995c2908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7f4f9dbf6f2371841cfe530c36b8341ca0772822038bd3983ca67428f477bf`

```dockerfile
```

-	Layers:
	-	`sha256:7964a06228d679e34749309df911e4f993cfdb332d28c9b0117e17e9a52c4197`  
		Last Modified: Tue, 04 Nov 2025 16:45:31 GMT  
		Size: 5.5 MB (5537004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9aa56bb8d72e1ec060d747be18da6e100963612bda5035ca87306b345192c5d`  
		Last Modified: Tue, 04 Nov 2025 16:45:32 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.5`

```console
$ docker pull ghost@sha256:337ce3180f977caa1a6c0fcd725395994cd580f622bfad1b2e2062cf7642a5cc
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

### `ghost:5.130.5` - linux; amd64

```console
$ docker pull ghost@sha256:f85733f3cbc898d36de4088f2fda14a125f8a49532ec00c7434cb8ea0e421f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb803bfa37a1461f5c31b8082c18f7b30fb4cafa2d430641d448228a6d4e34ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:34:32 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:34:32 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:32 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:34:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:43 GMT
CMD ["node"]
# Tue, 04 Nov 2025 04:33:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 04:33:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 04:33:50 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 04:33:50 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 04:34:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 04:35:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 04:35:07 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 04:35:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 04:35:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:35:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:35:07 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 04:35:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f707883943caee6170d1c96b0e24f29b11404bd9817e8e658e8c24898f94807`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9be599d8cff95c94bc0036ba643b354bfb691616e6f582ee79e08a20071764e`  
		Last Modified: Tue, 04 Nov 2025 00:35:04 GMT  
		Size: 41.0 MB (40977842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561299ddc92fb2324b06da8e6e176820a7eba31727bb4bc1cb1a28403ff4db12`  
		Last Modified: Tue, 04 Nov 2025 00:35:02 GMT  
		Size: 1.7 MB (1712619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7eb6b5a2b17e46a979515b9e341cce1eafc9b6035d440d435715fbb77690bb`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864aed93e665e6fa26d34620ea863882b848dc24e86f0fe197cdced4114e4562`  
		Last Modified: Tue, 04 Nov 2025 04:35:47 GMT  
		Size: 1.2 MB (1247537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba6c8fd4f450c1f7457c81998f7dd13f3010e3a4113093b112b454a1e2d09a4`  
		Last Modified: Tue, 04 Nov 2025 04:35:48 GMT  
		Size: 11.1 MB (11094147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3d3dff4aaa867d1ae255c80633027f39d66e5281984beb46805075f78e11a5`  
		Last Modified: Tue, 04 Nov 2025 04:35:54 GMT  
		Size: 118.0 MB (118018049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d29e5f38b1e0fa7e0f98cae6416943814b9a57577170b459e4451f1db9f44d`  
		Last Modified: Tue, 04 Nov 2025 04:35:47 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5` - unknown; unknown

```console
$ docker pull ghost@sha256:f4217b269e6c02f3b0044770a218ece6b4f9e62e2f2343af1989d7fb9fa0927f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f37142f2048af11deff44531397262046cfa9a752576896fac6401fdc4892e`

```dockerfile
```

-	Layers:
	-	`sha256:8c0305204fbc4eb1195f4a4532034b13bf62f90401195df4f47e23ef7aaf052c`  
		Last Modified: Tue, 04 Nov 2025 10:45:27 GMT  
		Size: 5.5 MB (5543181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4631011bb1a1306639afdeeb7e8acfe2dfbec54142e99360f5adcc478982daa3`  
		Last Modified: Tue, 04 Nov 2025 10:45:28 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:d54af2f62dbe59d10c76ec8b4c87eda9ba3e2a80e130a1270eaa7fd4b094048f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195612293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e008e162f1176295a864de55fd1777a3adbff9626cc579c97fbcce62b8501f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:46:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:47:03 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:47:03 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:47:03 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:47:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:47:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:47:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:47:15 GMT
CMD ["node"]
# Tue, 04 Nov 2025 02:43:46 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 02:43:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 02:43:46 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 02:43:46 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 02:44:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 02:46:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 02:46:49 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 02:46:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 02:46:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:46:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:46:49 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 02:46:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93c37c1fd1b7f4d09c483f03a2a845c305e3e3ecc99b3b52d68d46608ebb3f`  
		Last Modified: Tue, 04 Nov 2025 00:47:34 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7f2cf1babca77eeed4ac645ee2ed904d57e7ee6a13ff624054af478867074d`  
		Last Modified: Tue, 04 Nov 2025 00:47:38 GMT  
		Size: 37.1 MB (37064306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488f9e73958b5133b77535cce142f45578b4297a9b3554e3f83c569f3363b2f`  
		Last Modified: Tue, 04 Nov 2025 00:47:34 GMT  
		Size: 1.7 MB (1712823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb0f6234b40d280dd577f5ff6c58d1b026b669fdb3e89d6e96f2d5a1efcca7f`  
		Last Modified: Tue, 04 Nov 2025 00:47:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e8191b4d8b62dbbdb3ef3d4a6b899a6fede17cb071db5d2bbd145f29b88bd0`  
		Last Modified: Tue, 04 Nov 2025 02:47:32 GMT  
		Size: 1.2 MB (1214355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3102d25ad11605635394177f33ad305073fc8c0267601aadc4a9cbd9a68212`  
		Last Modified: Tue, 04 Nov 2025 02:47:33 GMT  
		Size: 11.1 MB (11094829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deeef39e9f4c1c4d9cf2263beb1ed290d522127aab93d27721ff9806f0a2fe5a`  
		Last Modified: Tue, 04 Nov 2025 02:47:44 GMT  
		Size: 120.6 MB (120587524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d66cc2862765c4676c6164d0f4ed12303ff5421ad0d8be8f792f1cd1b87ae7`  
		Last Modified: Tue, 04 Nov 2025 02:47:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5` - unknown; unknown

```console
$ docker pull ghost@sha256:940a9180000c1e68107a92ebdcfabeb0f181107cd9aa1df4cca5e768eb4ae1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d3cecb5fb064dc47a02da45dbfa06e6ec6cc4d8adb55e0694a81189ff25588`

```dockerfile
```

-	Layers:
	-	`sha256:d03259ddf9f5bea23fc228da9cad31e09474df6b009d025a60263281d9e6e3fa`  
		Last Modified: Tue, 04 Nov 2025 10:45:32 GMT  
		Size: 5.5 MB (5545960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bef53d686d15b6e964d4fa9cf4d4cea8735c5702804503b0776dc18ab6bfd45`  
		Last Modified: Tue, 04 Nov 2025 10:45:33 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b84f862c680ac2c30d07bc0b6c7ebdce04d4a85e0fd7045807073e95cc3a88e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201178174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3c609ac0e52a737db94f0a2a90d598558a4f2a5fd52f4c64ff045464a9d384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:23 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:35:42 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:35:42 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:42 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:35:53 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:35:53 GMT
CMD ["node"]
# Tue, 04 Nov 2025 01:48:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 01:48:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 01:48:51 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 01:48:51 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 01:49:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 01:50:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 01:50:19 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 01:50:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 01:50:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:50:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:50:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 01:50:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e3e431f7a520df14961d4498593d85568abcee7af80df09bfb1ecaef7cd45`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd1f8ab98ef1e2152eab9b695ec2f87db4d02435d64fdec15bd10a153ff849`  
		Last Modified: Tue, 04 Nov 2025 00:36:20 GMT  
		Size: 40.9 MB (40939662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaa03f4a05ff40bcfbe40175a2dbd854534498b254584994ed85d776bb55587`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 1.7 MB (1712633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6570b58c3e47b958ae4b68f789413ade8fe66580a20c717b3cb1e69f0c133ebf`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663ae620ac190c68e5d83a83b3d33b0eb2eb423a03fac16114cd3cd12cc5019f`  
		Last Modified: Tue, 04 Nov 2025 01:51:03 GMT  
		Size: 1.2 MB (1201430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9c0870ca41dfc91a0e2a298cdc47e8114d6f3d09c14d764b2d753f5f0670ce`  
		Last Modified: Tue, 04 Nov 2025 01:51:03 GMT  
		Size: 11.1 MB (11094919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602531b4420813b49243982ad8a1c2a9549dbae632743b32cb5a9805b2403887`  
		Last Modified: Tue, 04 Nov 2025 01:51:18 GMT  
		Size: 118.1 MB (118122828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295d0e4df7a9fe45640c39d05aa3a0c0eaaf7a3087e6211d12a3e53d0e9b6312`  
		Last Modified: Tue, 04 Nov 2025 01:51:02 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5` - unknown; unknown

```console
$ docker pull ghost@sha256:445ef3bc796bab18ada3fba661be331b721a771a43efdc88647eb5d116d4c68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5569425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4965280d091d4279629434307cdbaf3fb262b9134a9a4d73aab1897800946f`

```dockerfile
```

-	Layers:
	-	`sha256:067f8b997a5e51ef10a4601a130dfc95344c8ee4b8b4a912a5304279072e0562`  
		Last Modified: Tue, 04 Nov 2025 10:45:37 GMT  
		Size: 5.5 MB (5543508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:321b4338d423ea63134b074ba90c5d4d27bc35d8d7a43c0b0c1ddcc801008c85`  
		Last Modified: Tue, 04 Nov 2025 10:45:38 GMT  
		Size: 25.9 KB (25917 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5` - linux; s390x

```console
$ docker pull ghost@sha256:fedc92789cc63ec80586657b88fa4c694f5ef240cd4f4a2b6c1688440c7a4439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204802905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c301e77ea9647ac3183392844f94ef4ebc65b70ae40551ea9eadc7d1b9625a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:33:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 03:37:01 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 03:37:01 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:37:01 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 03:37:10 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:37:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:37:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:37:10 GMT
CMD ["node"]
# Tue, 04 Nov 2025 13:34:35 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 13:34:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 13:34:35 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 13:34:35 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 13:34:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 13:37:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 13:37:13 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 13:37:13 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 13:37:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 13:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 13:37:13 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 13:37:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b483b0df66cd8c70ba210c61fdc3840348da24bad86177f3799a15a254e527`  
		Last Modified: Tue, 04 Nov 2025 03:34:01 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a391e545ed0d8aeddbbfdf6c58840bd79044b2d7724a7f9e2f4b25f94cd446`  
		Last Modified: Tue, 04 Nov 2025 03:37:41 GMT  
		Size: 41.2 MB (41222577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff94fd9f029756b1291b5b34bfc358a41e9c02a77d415cf91c92e6480c8cc12`  
		Last Modified: Tue, 04 Nov 2025 03:37:39 GMT  
		Size: 1.7 MB (1712621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb828a655db1ab796ec4ec301dbddaed50020b282af492e0ad200dcd1a7f9a7`  
		Last Modified: Tue, 04 Nov 2025 03:37:39 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f328b3f0fc2f5ec6a0ce9d45ffce274cdc93a98a55cd8eaaa4d1cb295fb11a`  
		Last Modified: Tue, 04 Nov 2025 13:38:12 GMT  
		Size: 1.2 MB (1221301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84250905d6e664f6e19a3907889c1832e155c4a9e639f732621d0ad78b5eea0f`  
		Last Modified: Tue, 04 Nov 2025 13:38:15 GMT  
		Size: 11.1 MB (11093207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaf51cd926003ef4b173028a768cbd8235b7fab10f8364c526e52155d74609b`  
		Last Modified: Tue, 04 Nov 2025 13:38:22 GMT  
		Size: 122.7 MB (122664325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002ebcdf1e703e7b6e8e6dedf4cff0aba49d24404fce1007cd77b34af1011f7c`  
		Last Modified: Tue, 04 Nov 2025 13:38:12 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5` - unknown; unknown

```console
$ docker pull ghost@sha256:aea28f5f061e7e1fe6c72475dc569a1ff0dcf919d99e365cb48cd601995c2908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7f4f9dbf6f2371841cfe530c36b8341ca0772822038bd3983ca67428f477bf`

```dockerfile
```

-	Layers:
	-	`sha256:7964a06228d679e34749309df911e4f993cfdb332d28c9b0117e17e9a52c4197`  
		Last Modified: Tue, 04 Nov 2025 16:45:31 GMT  
		Size: 5.5 MB (5537004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9aa56bb8d72e1ec060d747be18da6e100963612bda5035ca87306b345192c5d`  
		Last Modified: Tue, 04 Nov 2025 16:45:32 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.5-alpine`

```console
$ docker pull ghost@sha256:6cca0c2a8a2ca5f57e31bf311e8c35b570be0b0c2451c9c37bea55197bdfeb68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130.5-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:0f70a24b1ba6a1d3997eaf4853a6e6f6d6fafb0446c28f3deeaf3a01252423f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175511698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68920e05396cd4669b7e3c46d22a38fb4333b55009f4ea79fa4b6209db38440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:24 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:14:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:14:26 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:14:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:14:26 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:14:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e45a9660cfaebbbac9bba98180aa28b3966b7f2462d132c46f51a1f5b25a64`  
		Last Modified: Tue, 21 Oct 2025 20:19:28 GMT  
		Size: 42.8 MB (42750841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74e4ed823e9560b3fe51c0cab47dbfdfc4b12453604319408ec58708fb9e720`  
		Last Modified: Tue, 21 Oct 2025 20:19:17 GMT  
		Size: 1.3 MB (1260590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04d522c98fe12816b2bcddf8413fca73645f8fa60f287c672f58bcc7f0fa38`  
		Last Modified: Tue, 21 Oct 2025 20:19:16 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0f9a897060feb550287b8d83fcf4ee55da3c30f54db1edf978b006db787df`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 777.0 KB (777045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b382b367f507fc850a39a16fec12749f6c1306dc08e0e4f5d9fb4e9fb87140`  
		Last Modified: Mon, 03 Nov 2025 23:15:08 GMT  
		Size: 923.4 KB (923439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4892805e65559d25032860f128b6ffde24688439b15eafae4582e7433248835`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be658ce9c8e59f7aa9d714b669e868cc97bb892900145e917445a00f7684af`  
		Last Modified: Mon, 03 Nov 2025 23:15:09 GMT  
		Size: 11.1 MB (11093048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67e9dd34d742b7cb05cf61410a70c7992f27db78d903721c0c4cb0550b4883`  
		Last Modified: Mon, 03 Nov 2025 23:15:17 GMT  
		Size: 114.9 MB (114903085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa3dd720a5026dbd84f0306d99be03e7e0f6481b674c2a664c60743d5b0bf5`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:0705a01a45b41466c233e6ff85abb3245f22f31baa322462468a6c9d259c7ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5c4812ee7cd0ae829317bd459870791c1165f3b1ece1398199ae4792524700`

```dockerfile
```

-	Layers:
	-	`sha256:1210e51ac71ad4e5f3362abb7b760cf9634edaa2629be743b66e7e65cc2bf36d`  
		Last Modified: Tue, 04 Nov 2025 01:45:24 GMT  
		Size: 3.3 MB (3330079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e4429e809841d6839249a064f9f674748ca2445fab5bbf04eeabf3c5053ace`  
		Last Modified: Tue, 04 Nov 2025 01:45:25 GMT  
		Size: 28.3 KB (28295 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:86bf1443622143bb16bee447fe4c778ad3e965699ee809c01355752173c0923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186152453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3311524bf8d21f721e8381834f51617e7085c55d1156e168336a952037c0819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:41 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:15:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:15:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:15:00 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:15:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae67534e7d0aa8a27cfb7e3ecb9727f2ce2a6dd5b721d5392c27b91fc68b7f13`  
		Last Modified: Tue, 21 Oct 2025 19:27:20 GMT  
		Size: 42.4 MB (42425867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf56a7feaf43fe338cd74317fda62608ec88dfd616dd5bff62f6f11b631692`  
		Last Modified: Tue, 21 Oct 2025 19:27:16 GMT  
		Size: 1.3 MB (1260570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dae84293a5e75bd15077274b31b14eaec6c0fc94e035b36febae220198d1f2`  
		Last Modified: Tue, 21 Oct 2025 19:27:15 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a9c55bf6a0924e65b32510d0961685bdd8d8f2b10c2db7dd7c96bdd51bf6a9`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 838.6 KB (838585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6208bc17bacacf9b675576e3a0f1ea6703a538aa99a36a8afc4f265ad6606fd4`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e145e2590cb18e81ffe8ac9d21e865b79a70aae4f5cf913d72227d6b5a0c89f`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5e151584a8a323c8c95a64b09e39e356af36f4eaafda1e33ccbd47f82ccb9c`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 11.1 MB (11094690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea721408dbea49d2025fa1a9c571d38cb1fc8f275fc6505f5dad38b4f7f0f44`  
		Last Modified: Mon, 03 Nov 2025 23:16:00 GMT  
		Size: 125.5 MB (125517109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df139f51032436062d10fd724eba3c899f0f3c8bdb77226d7140ecfcc55e6308`  
		Last Modified: Mon, 03 Nov 2025 23:15:47 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:d3def10dd533d48e2cbbf4453012f2197ed4d09a6cfb48880f830a1436e526e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e2fa9bacdd7216a338861d1c288ae6ee8a60f4fc28c1105ec3906ebeb554a2`

```dockerfile
```

-	Layers:
	-	`sha256:32d63c33bb3db7b0d81adf8e25e21c55071e4fe60e7e4a74d6191983d7d6b88b`  
		Last Modified: Tue, 04 Nov 2025 01:45:29 GMT  
		Size: 3.3 MB (3330211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abbb7369c2dac9f8713988834f81b90112f90d7083f3f254112a5711ac640346`  
		Last Modified: Tue, 04 Nov 2025 01:45:30 GMT  
		Size: 28.5 KB (28483 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.5-alpine3.22`

```console
$ docker pull ghost@sha256:6cca0c2a8a2ca5f57e31bf311e8c35b570be0b0c2451c9c37bea55197bdfeb68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130.5-alpine3.22` - linux; amd64

```console
$ docker pull ghost@sha256:0f70a24b1ba6a1d3997eaf4853a6e6f6d6fafb0446c28f3deeaf3a01252423f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175511698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68920e05396cd4669b7e3c46d22a38fb4333b55009f4ea79fa4b6209db38440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:24 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:26 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:26 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:36 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:36 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:14:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:14:26 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:14:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:14:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:14:26 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:14:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e45a9660cfaebbbac9bba98180aa28b3966b7f2462d132c46f51a1f5b25a64`  
		Last Modified: Tue, 21 Oct 2025 20:19:28 GMT  
		Size: 42.8 MB (42750841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74e4ed823e9560b3fe51c0cab47dbfdfc4b12453604319408ec58708fb9e720`  
		Last Modified: Tue, 21 Oct 2025 20:19:17 GMT  
		Size: 1.3 MB (1260590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04d522c98fe12816b2bcddf8413fca73645f8fa60f287c672f58bcc7f0fa38`  
		Last Modified: Tue, 21 Oct 2025 20:19:16 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0f9a897060feb550287b8d83fcf4ee55da3c30f54db1edf978b006db787df`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 777.0 KB (777045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b382b367f507fc850a39a16fec12749f6c1306dc08e0e4f5d9fb4e9fb87140`  
		Last Modified: Mon, 03 Nov 2025 23:15:08 GMT  
		Size: 923.4 KB (923439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4892805e65559d25032860f128b6ffde24688439b15eafae4582e7433248835`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be658ce9c8e59f7aa9d714b669e868cc97bb892900145e917445a00f7684af`  
		Last Modified: Mon, 03 Nov 2025 23:15:09 GMT  
		Size: 11.1 MB (11093048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67e9dd34d742b7cb05cf61410a70c7992f27db78d903721c0c4cb0550b4883`  
		Last Modified: Mon, 03 Nov 2025 23:15:17 GMT  
		Size: 114.9 MB (114903085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefa3dd720a5026dbd84f0306d99be03e7e0f6481b674c2a664c60743d5b0bf5`  
		Last Modified: Mon, 03 Nov 2025 23:15:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:0705a01a45b41466c233e6ff85abb3245f22f31baa322462468a6c9d259c7ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5c4812ee7cd0ae829317bd459870791c1165f3b1ece1398199ae4792524700`

```dockerfile
```

-	Layers:
	-	`sha256:1210e51ac71ad4e5f3362abb7b760cf9634edaa2629be743b66e7e65cc2bf36d`  
		Last Modified: Tue, 04 Nov 2025 01:45:24 GMT  
		Size: 3.3 MB (3330079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e4429e809841d6839249a064f9f674748ca2445fab5bbf04eeabf3c5053ace`  
		Last Modified: Tue, 04 Nov 2025 01:45:25 GMT  
		Size: 28.3 KB (28295 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:86bf1443622143bb16bee447fe4c778ad3e965699ee809c01355752173c0923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186152453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3311524bf8d21f721e8381834f51617e7085c55d1156e168336a952037c0819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
# Mon, 03 Nov 2025 23:13:25 GMT
RUN apk add --no-cache 		bash # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility # buildkit
# Mon, 03 Nov 2025 23:13:28 GMT
ENV NODE_ENV=production
# Mon, 03 Nov 2025 23:13:28 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Mon, 03 Nov 2025 23:13:41 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Mon, 03 Nov 2025 23:13:41 GMT
ENV GHOST_VERSION=5.130.5
# Mon, 03 Nov 2025 23:15:00 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
WORKDIR /var/lib/ghost
# Mon, 03 Nov 2025 23:15:00 GMT
VOLUME [/var/lib/ghost/content]
# Mon, 03 Nov 2025 23:15:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 23:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 23:15:00 GMT
EXPOSE map[2368/tcp:{}]
# Mon, 03 Nov 2025 23:15:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae67534e7d0aa8a27cfb7e3ecb9727f2ce2a6dd5b721d5392c27b91fc68b7f13`  
		Last Modified: Tue, 21 Oct 2025 19:27:20 GMT  
		Size: 42.4 MB (42425867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf56a7feaf43fe338cd74317fda62608ec88dfd616dd5bff62f6f11b631692`  
		Last Modified: Tue, 21 Oct 2025 19:27:16 GMT  
		Size: 1.3 MB (1260570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dae84293a5e75bd15077274b31b14eaec6c0fc94e035b36febae220198d1f2`  
		Last Modified: Tue, 21 Oct 2025 19:27:15 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a9c55bf6a0924e65b32510d0961685bdd8d8f2b10c2db7dd7c96bdd51bf6a9`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 838.6 KB (838585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6208bc17bacacf9b675576e3a0f1ea6703a538aa99a36a8afc4f265ad6606fd4`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e145e2590cb18e81ffe8ac9d21e865b79a70aae4f5cf913d72227d6b5a0c89f`  
		Last Modified: Mon, 03 Nov 2025 23:15:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5e151584a8a323c8c95a64b09e39e356af36f4eaafda1e33ccbd47f82ccb9c`  
		Last Modified: Mon, 03 Nov 2025 23:15:45 GMT  
		Size: 11.1 MB (11094690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea721408dbea49d2025fa1a9c571d38cb1fc8f275fc6505f5dad38b4f7f0f44`  
		Last Modified: Mon, 03 Nov 2025 23:16:00 GMT  
		Size: 125.5 MB (125517109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df139f51032436062d10fd724eba3c899f0f3c8bdb77226d7140ecfcc55e6308`  
		Last Modified: Mon, 03 Nov 2025 23:15:47 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:d3def10dd533d48e2cbbf4453012f2197ed4d09a6cfb48880f830a1436e526e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e2fa9bacdd7216a338861d1c288ae6ee8a60f4fc28c1105ec3906ebeb554a2`

```dockerfile
```

-	Layers:
	-	`sha256:32d63c33bb3db7b0d81adf8e25e21c55071e4fe60e7e4a74d6191983d7d6b88b`  
		Last Modified: Tue, 04 Nov 2025 01:45:29 GMT  
		Size: 3.3 MB (3330211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abbb7369c2dac9f8713988834f81b90112f90d7083f3f254112a5711ac640346`  
		Last Modified: Tue, 04 Nov 2025 01:45:30 GMT  
		Size: 28.5 KB (28483 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.5-bookworm`

```console
$ docker pull ghost@sha256:337ce3180f977caa1a6c0fcd725395994cd580f622bfad1b2e2062cf7642a5cc
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

### `ghost:5.130.5-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:f85733f3cbc898d36de4088f2fda14a125f8a49532ec00c7434cb8ea0e421f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb803bfa37a1461f5c31b8082c18f7b30fb4cafa2d430641d448228a6d4e34ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:12 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:34:32 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:34:32 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:32 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:34:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:43 GMT
CMD ["node"]
# Tue, 04 Nov 2025 04:33:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 04:33:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 04:33:50 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 04:33:50 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 04:34:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 04:34:01 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 04:35:07 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 04:35:07 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 04:35:07 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 04:35:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:35:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:35:07 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 04:35:07 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f707883943caee6170d1c96b0e24f29b11404bd9817e8e658e8c24898f94807`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9be599d8cff95c94bc0036ba643b354bfb691616e6f582ee79e08a20071764e`  
		Last Modified: Tue, 04 Nov 2025 00:35:04 GMT  
		Size: 41.0 MB (40977842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561299ddc92fb2324b06da8e6e176820a7eba31727bb4bc1cb1a28403ff4db12`  
		Last Modified: Tue, 04 Nov 2025 00:35:02 GMT  
		Size: 1.7 MB (1712619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7eb6b5a2b17e46a979515b9e341cce1eafc9b6035d440d435715fbb77690bb`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864aed93e665e6fa26d34620ea863882b848dc24e86f0fe197cdced4114e4562`  
		Last Modified: Tue, 04 Nov 2025 04:35:47 GMT  
		Size: 1.2 MB (1247537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba6c8fd4f450c1f7457c81998f7dd13f3010e3a4113093b112b454a1e2d09a4`  
		Last Modified: Tue, 04 Nov 2025 04:35:48 GMT  
		Size: 11.1 MB (11094147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3d3dff4aaa867d1ae255c80633027f39d66e5281984beb46805075f78e11a5`  
		Last Modified: Tue, 04 Nov 2025 04:35:54 GMT  
		Size: 118.0 MB (118018049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d29e5f38b1e0fa7e0f98cae6416943814b9a57577170b459e4451f1db9f44d`  
		Last Modified: Tue, 04 Nov 2025 04:35:47 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:f4217b269e6c02f3b0044770a218ece6b4f9e62e2f2343af1989d7fb9fa0927f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f37142f2048af11deff44531397262046cfa9a752576896fac6401fdc4892e`

```dockerfile
```

-	Layers:
	-	`sha256:8c0305204fbc4eb1195f4a4532034b13bf62f90401195df4f47e23ef7aaf052c`  
		Last Modified: Tue, 04 Nov 2025 10:45:27 GMT  
		Size: 5.5 MB (5543181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4631011bb1a1306639afdeeb7e8acfe2dfbec54142e99360f5adcc478982daa3`  
		Last Modified: Tue, 04 Nov 2025 10:45:28 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:d54af2f62dbe59d10c76ec8b4c87eda9ba3e2a80e130a1270eaa7fd4b094048f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195612293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e008e162f1176295a864de55fd1777a3adbff9626cc579c97fbcce62b8501f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:46:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:47:03 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:47:03 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:47:03 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:47:15 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:47:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:47:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:47:15 GMT
CMD ["node"]
# Tue, 04 Nov 2025 02:43:46 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 02:43:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 02:43:46 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 02:43:46 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 02:44:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 02:44:00 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 02:46:49 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 02:46:49 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 02:46:49 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 02:46:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:46:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:46:49 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 02:46:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93c37c1fd1b7f4d09c483f03a2a845c305e3e3ecc99b3b52d68d46608ebb3f`  
		Last Modified: Tue, 04 Nov 2025 00:47:34 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7f2cf1babca77eeed4ac645ee2ed904d57e7ee6a13ff624054af478867074d`  
		Last Modified: Tue, 04 Nov 2025 00:47:38 GMT  
		Size: 37.1 MB (37064306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488f9e73958b5133b77535cce142f45578b4297a9b3554e3f83c569f3363b2f`  
		Last Modified: Tue, 04 Nov 2025 00:47:34 GMT  
		Size: 1.7 MB (1712823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb0f6234b40d280dd577f5ff6c58d1b026b669fdb3e89d6e96f2d5a1efcca7f`  
		Last Modified: Tue, 04 Nov 2025 00:47:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e8191b4d8b62dbbdb3ef3d4a6b899a6fede17cb071db5d2bbd145f29b88bd0`  
		Last Modified: Tue, 04 Nov 2025 02:47:32 GMT  
		Size: 1.2 MB (1214355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3102d25ad11605635394177f33ad305073fc8c0267601aadc4a9cbd9a68212`  
		Last Modified: Tue, 04 Nov 2025 02:47:33 GMT  
		Size: 11.1 MB (11094829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deeef39e9f4c1c4d9cf2263beb1ed290d522127aab93d27721ff9806f0a2fe5a`  
		Last Modified: Tue, 04 Nov 2025 02:47:44 GMT  
		Size: 120.6 MB (120587524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d66cc2862765c4676c6164d0f4ed12303ff5421ad0d8be8f792f1cd1b87ae7`  
		Last Modified: Tue, 04 Nov 2025 02:47:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:940a9180000c1e68107a92ebdcfabeb0f181107cd9aa1df4cca5e768eb4ae1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d3cecb5fb064dc47a02da45dbfa06e6ec6cc4d8adb55e0694a81189ff25588`

```dockerfile
```

-	Layers:
	-	`sha256:d03259ddf9f5bea23fc228da9cad31e09474df6b009d025a60263281d9e6e3fa`  
		Last Modified: Tue, 04 Nov 2025 10:45:32 GMT  
		Size: 5.5 MB (5545960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bef53d686d15b6e964d4fa9cf4d4cea8735c5702804503b0776dc18ab6bfd45`  
		Last Modified: Tue, 04 Nov 2025 10:45:33 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:b84f862c680ac2c30d07bc0b6c7ebdce04d4a85e0fd7045807073e95cc3a88e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201178174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3c609ac0e52a737db94f0a2a90d598558a4f2a5fd52f4c64ff045464a9d384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:23 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:35:42 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 00:35:42 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:42 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:35:53 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:35:53 GMT
CMD ["node"]
# Tue, 04 Nov 2025 01:48:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 01:48:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 01:48:51 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 01:48:51 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 01:49:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 01:49:05 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 01:50:19 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 01:50:19 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 01:50:19 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 01:50:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:50:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:50:19 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 01:50:19 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e3e431f7a520df14961d4498593d85568abcee7af80df09bfb1ecaef7cd45`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd1f8ab98ef1e2152eab9b695ec2f87db4d02435d64fdec15bd10a153ff849`  
		Last Modified: Tue, 04 Nov 2025 00:36:20 GMT  
		Size: 40.9 MB (40939662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaa03f4a05ff40bcfbe40175a2dbd854534498b254584994ed85d776bb55587`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 1.7 MB (1712633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6570b58c3e47b958ae4b68f789413ade8fe66580a20c717b3cb1e69f0c133ebf`  
		Last Modified: Tue, 04 Nov 2025 00:36:15 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663ae620ac190c68e5d83a83b3d33b0eb2eb423a03fac16114cd3cd12cc5019f`  
		Last Modified: Tue, 04 Nov 2025 01:51:03 GMT  
		Size: 1.2 MB (1201430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9c0870ca41dfc91a0e2a298cdc47e8114d6f3d09c14d764b2d753f5f0670ce`  
		Last Modified: Tue, 04 Nov 2025 01:51:03 GMT  
		Size: 11.1 MB (11094919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602531b4420813b49243982ad8a1c2a9549dbae632743b32cb5a9805b2403887`  
		Last Modified: Tue, 04 Nov 2025 01:51:18 GMT  
		Size: 118.1 MB (118122828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295d0e4df7a9fe45640c39d05aa3a0c0eaaf7a3087e6211d12a3e53d0e9b6312`  
		Last Modified: Tue, 04 Nov 2025 01:51:02 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:445ef3bc796bab18ada3fba661be331b721a771a43efdc88647eb5d116d4c68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5569425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4965280d091d4279629434307cdbaf3fb262b9134a9a4d73aab1897800946f`

```dockerfile
```

-	Layers:
	-	`sha256:067f8b997a5e51ef10a4601a130dfc95344c8ee4b8b4a912a5304279072e0562`  
		Last Modified: Tue, 04 Nov 2025 10:45:37 GMT  
		Size: 5.5 MB (5543508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:321b4338d423ea63134b074ba90c5d4d27bc35d8d7a43c0b0c1ddcc801008c85`  
		Last Modified: Tue, 04 Nov 2025 10:45:38 GMT  
		Size: 25.9 KB (25917 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.5-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:fedc92789cc63ec80586657b88fa4c694f5ef240cd4f4a2b6c1688440c7a4439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204802905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c301e77ea9647ac3183392844f94ef4ebc65b70ae40551ea9eadc7d1b9625a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:33:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 03:37:01 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 03:37:01 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:37:01 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 03:37:10 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:37:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:37:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:37:10 GMT
CMD ["node"]
# Tue, 04 Nov 2025 13:34:35 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 13:34:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 13:34:35 GMT
ENV NODE_ENV=production
# Tue, 04 Nov 2025 13:34:35 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Tue, 04 Nov 2025 13:34:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 04 Nov 2025 13:34:54 GMT
ENV GHOST_VERSION=5.130.5
# Tue, 04 Nov 2025 13:37:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Tue, 04 Nov 2025 13:37:13 GMT
WORKDIR /var/lib/ghost
# Tue, 04 Nov 2025 13:37:13 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 04 Nov 2025 13:37:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 13:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 13:37:13 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 04 Nov 2025 13:37:13 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b483b0df66cd8c70ba210c61fdc3840348da24bad86177f3799a15a254e527`  
		Last Modified: Tue, 04 Nov 2025 03:34:01 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a391e545ed0d8aeddbbfdf6c58840bd79044b2d7724a7f9e2f4b25f94cd446`  
		Last Modified: Tue, 04 Nov 2025 03:37:41 GMT  
		Size: 41.2 MB (41222577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff94fd9f029756b1291b5b34bfc358a41e9c02a77d415cf91c92e6480c8cc12`  
		Last Modified: Tue, 04 Nov 2025 03:37:39 GMT  
		Size: 1.7 MB (1712621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb828a655db1ab796ec4ec301dbddaed50020b282af492e0ad200dcd1a7f9a7`  
		Last Modified: Tue, 04 Nov 2025 03:37:39 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f328b3f0fc2f5ec6a0ce9d45ffce274cdc93a98a55cd8eaaa4d1cb295fb11a`  
		Last Modified: Tue, 04 Nov 2025 13:38:12 GMT  
		Size: 1.2 MB (1221301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84250905d6e664f6e19a3907889c1832e155c4a9e639f732621d0ad78b5eea0f`  
		Last Modified: Tue, 04 Nov 2025 13:38:15 GMT  
		Size: 11.1 MB (11093207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaf51cd926003ef4b173028a768cbd8235b7fab10f8364c526e52155d74609b`  
		Last Modified: Tue, 04 Nov 2025 13:38:22 GMT  
		Size: 122.7 MB (122664325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002ebcdf1e703e7b6e8e6dedf4cff0aba49d24404fce1007cd77b34af1011f7c`  
		Last Modified: Tue, 04 Nov 2025 13:38:12 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:aea28f5f061e7e1fe6c72475dc569a1ff0dcf919d99e365cb48cd601995c2908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7f4f9dbf6f2371841cfe530c36b8341ca0772822038bd3983ca67428f477bf`

```dockerfile
```

-	Layers:
	-	`sha256:7964a06228d679e34749309df911e4f993cfdb332d28c9b0117e17e9a52c4197`  
		Last Modified: Tue, 04 Nov 2025 16:45:31 GMT  
		Size: 5.5 MB (5537004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9aa56bb8d72e1ec060d747be18da6e100963612bda5035ca87306b345192c5d`  
		Last Modified: Tue, 04 Nov 2025 16:45:32 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6`

```console
$ docker pull ghost@sha256:85e15524ac7e437720fa4ac3cd4633daaae3f95786a25633415d8d4f7382b4c4
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
$ docker pull ghost@sha256:d6305ad973dec2adb1e34dc71e2306e677e9ae485826162435740e12138b353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220013893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0657b74d11a9a245eda88cdd14a1a2af921eb72358fa1f1d0e7474032933fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:34:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:34:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:37 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:15:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:15:05 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:09 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:09 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427deb858cffe936256f73e134a5baf1b4a26a93b79e03850d2243f6bc1fb302`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d65a4ff088ddf61684b1496e527c5c3accd5af20974f6dd6c3bc58a93412dc`  
		Last Modified: Tue, 04 Nov 2025 00:35:04 GMT  
		Size: 49.5 MB (49481524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6653fee0b024a9e265d5b1d360a35e40e56d7b2212c51acbf76e66c88af4e02`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 1.7 MB (1712601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b7c6f7614440681a3a5b71d3914a7eb7f5122582683ae69e336cd32f238a04`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30f248c587c9e58ca2ee47211c48b240ad9159d324a31e252758ff18b68f77`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 1.2 MB (1247558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44211e7148bae27b3894b362a850d7dd095fdafa9dbea2175f94f7a7c15ce16a`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 11.7 MB (11661069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d95e3f22588236ed74154b6d0a33a31eec2d368e9bf05f8d032fca21638741`  
		Last Modified: Fri, 14 Nov 2025 17:18:22 GMT  
		Size: 127.7 MB (127678242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77aecbe65670514cc189a958e46c069c5bfbf80f12976df53de71d4d0513f8e`  
		Last Modified: Fri, 14 Nov 2025 17:18:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:c9996812fd0e5f37e9e2b5d4bd78dec441a03998d6c7100ae32c1daea95cb9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ac2c21a42e31f5bb89ef9098d4858bf42da1e90c4699c1703c011bf04abce5`

```dockerfile
```

-	Layers:
	-	`sha256:411dbbbb7b2789695a3de35dc7167e3c3a9eaa2b74d7cb01ed3765fc5f2d0bbb`  
		Last Modified: Fri, 14 Nov 2025 19:45:37 GMT  
		Size: 5.6 MB (5610690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f4880ee6e04ecce1050ea974cb0796306623dfc25b6c84f155486f5f2aae4d`  
		Last Modified: Fri, 14 Nov 2025 19:45:38 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm variant v7

```console
$ docker pull ghost@sha256:6fb588205dea09931300802a570cafedb86a09af55a54c3d750c34a2b90cede7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211470991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b993d5a857428e277dd35f395d4c38e1d228abefb335b477aa9ff18cdcd8f5a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:45:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:45:27 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:45:40 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:45:40 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:13:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:13:35 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:48 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:49 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:49 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4e79d7f6a82ac834b2b909c91adf66e2efc1389b7e127d8b803cd2a3f7c095`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce593c94118d14798314e3d79e0dfbe9a2a25e8fb36f3d425e2ac3f0aac86b80`  
		Last Modified: Tue, 04 Nov 2025 00:46:06 GMT  
		Size: 44.2 MB (44208200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6316a5dddcba87433a3ac4218d745b63913b646e0d8e387ce926ce0088397de5`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 1.7 MB (1712839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832c6ea2913823d440451db9e0d70234cfb8cd353410b97f145c0fb0a102c2d6`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9751750267a6b953a3de587887881044849607b480b85b892f2d5ab40d6181`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 1.2 MB (1214409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f797f5f0b4bb007779916de8ee6d37f7f5869bd2ace21c9e163299a6c84f4037`  
		Last Modified: Fri, 14 Nov 2025 17:17:50 GMT  
		Size: 11.7 MB (11660119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db2a424c497982a7352c6bd346313619705728b03b78e2e6363e76f063ff134`  
		Last Modified: Fri, 14 Nov 2025 20:23:39 GMT  
		Size: 128.7 MB (128736966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad36ca1c9c94347ef2e30f86a8a83344aac769110da5d73334406f3e67d3f18`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:68ae07f1cddb025b203c7329731967c2376f075be3f4506dd4c64d6882201c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd78e61405dd7e6c2f94c2cc81bec597f4756c28054a64ea6219ebfe84d1616`

```dockerfile
```

-	Layers:
	-	`sha256:37c3534eccf25aa343a7c345cd9ed2999640c0d231082055410e5e084cafd22f`  
		Last Modified: Fri, 14 Nov 2025 19:45:43 GMT  
		Size: 5.6 MB (5613489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e62a0ec9c3265208738ffd9a496a6ddd90aef3e2db9e96d344dc51c15b6e875`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 26.5 KB (26472 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:8d6f3599b40431c17606f590240838ffa35effe0109f502d2543b5c835346784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220075003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb2d4a30d3be8fb6084ffbdefd94aab83b46cf63d4ab0e0ff3e79e563436612`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:35:35 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:35:46 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:35:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:48 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:27 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce654a657d29e2be7faa623cc5a1877b6a78e8b6669ef6e9e48a54b261f2dbb1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36115b3c0ec4b3e7a273bca9f36591f9b2db12432bf4f70ad0f38fee26d12353`  
		Last Modified: Tue, 04 Nov 2025 00:36:13 GMT  
		Size: 49.6 MB (49614672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53479a8a7fd9dfad5cc88f68b7182c993f5e24b6cfc0b672e3c96b28eadc3da9`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be8e8db985232f1716a04e833933730acd9419ec49aa51c1f1aa69fe22888e1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29f9b4dcd7e856a096ca07550a76b23003c52689d12394cb194daf637fd35e8`  
		Last Modified: Fri, 14 Nov 2025 17:18:45 GMT  
		Size: 1.2 MB (1201445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e917f52639864038fbd445a1047ab571f36715192e655b1d5e33925a16354f`  
		Last Modified: Fri, 14 Nov 2025 17:18:46 GMT  
		Size: 11.7 MB (11666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567d8828b01841392dcf0dec341fe287fbf97ce1e1929e6e32dd8695d51b257d`  
		Last Modified: Fri, 14 Nov 2025 17:19:04 GMT  
		Size: 127.8 MB (127772964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3222ac9c7fc4d2dd2ab35916c7a28642609a55b223c5157379fb85bc15a2cebd`  
		Last Modified: Fri, 14 Nov 2025 17:18:44 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:56215ea56599da1bac73faf28a96259dc0479ae63a86ff364bbd90dcc7724e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6adac70a75f2b20757743143591caa6e38377ba58f3a19bc2720bc0c8de3073`

```dockerfile
```

-	Layers:
	-	`sha256:d1a67ed51384953de0b80812877aeafa3ab4d77d73b8d3a65a991d1c6567d6fa`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 5.6 MB (5611041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2e739425d1eef4534729048ffb99a1cfef0b1f96ea1ce2b896b9694bc38cbc5`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.5 KB (26516 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; s390x

```console
$ docker pull ghost@sha256:cfd3d21d5e1501f362a50c090a0dfebfdbdbfb6a5251c68cc7866c581447b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221995814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483f844dc2b67fe79f4cc732a0b6547572e68c3e37e1660755d293490e38fa75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:33:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 03:35:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 03:35:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:35:48 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:21 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:39 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:43 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:43 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:43 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:44 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b483b0df66cd8c70ba210c61fdc3840348da24bad86177f3799a15a254e527`  
		Last Modified: Tue, 04 Nov 2025 03:34:01 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b320a6187066ba76389a7c79a1ddcb01d2b7798c2b10f4a370838218e2b7502`  
		Last Modified: Tue, 04 Nov 2025 03:36:30 GMT  
		Size: 49.7 MB (49676869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94b7e8c1441d6d3f81305d6be716fd246c56e2ffe42813414eee448bcc0db3d`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b080f614a4846400e9341eea05bfc895791733a0574b3b7a0e133f7095e26c3b`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e25b4aea4e283179ce72acb52f272e26fdc644f71a2f31d91ce19c7cb83c9a4`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 1.2 MB (1221305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b5b430011654539652162ae126fad71141236f36f4bd289668bffd636e4597`  
		Last Modified: Fri, 14 Nov 2025 17:17:56 GMT  
		Size: 11.7 MB (11676181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffba5d1b26178851461a6d7112f84646693457b752e5ee763672efed2aaa2013`  
		Last Modified: Fri, 14 Nov 2025 17:17:37 GMT  
		Size: 130.8 MB (130819971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1617d5b92e47b9096b44c75075adef4bb47445928af5b155ae01683c2375062d`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:00547a5deba99ed2a3feaf2c865feeb31da0b741f8dad07caae3b66249f9725b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c118fdb5d65f98f9c554f78161e9cd1326cbbbbbba84d9a10d93e9a76b1a48d6`

```dockerfile
```

-	Layers:
	-	`sha256:62eab9ad244f580d8fcab14bd3eccf3e0196228bd3ccac84cf7b891b8c28b586`  
		Last Modified: Fri, 14 Nov 2025 19:45:55 GMT  
		Size: 5.6 MB (5604517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc702032869af479006fa83b52bb022c5877562d2508f26b9380b61b2e3264`  
		Last Modified: Fri, 14 Nov 2025 19:45:56 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine`

```console
$ docker pull ghost@sha256:b336036a044d6e0f38427725ce777555ca05bcbefa9d51761c962edcf91242f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:e20b75ba2535eb71b1f05f87b00d526b2832c5dca8ae9fac2b06255b8fcb0110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197462745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac976d839b348c5f7aabae4bb681c0febefa62da0eb864d526b44d77adffc28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:16:03 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:16:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:03 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:16:06 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:16:06 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:17:09 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:17:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2cca81d0de31536e59c1e347c529041866e5f6e73effbcd570f0373d4fbaf7`  
		Last Modified: Wed, 29 Oct 2025 14:16:30 GMT  
		Size: 51.6 MB (51567005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1acb8d81a6ae3f5871ce734e5b9aabd5cdb01ccb4fe07ec71c33d75bb4eb04c`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 1.3 MB (1260587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff8b913658cef54b13151d83455a1387472901b28d1f6a0adc49beb04b26ddc`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93780dcece6a389ee0fc2878ac73de722b82d44e5236349ad8019e4f57740dca`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 777.0 KB (777046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb03a2b21b7dd47b4be8e6dc3389204c91156dacd3f6a797875e0665097340`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 923.4 KB (923436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305212959a3c0bcac2d57cf3c9fa68eab4685f0849724388c08c54074e887411`  
		Last Modified: Fri, 14 Nov 2025 17:20:13 GMT  
		Size: 11.7 MB (11661070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f1d5752b1a9e4b15a37f485ed95d8e815fd7560631d635d94bc1870b8c024d`  
		Last Modified: Fri, 14 Nov 2025 17:20:23 GMT  
		Size: 127.5 MB (127470132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59a81117abbc6765eba809e22fab73ba2bf0a860700d424f912640757b34968`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c40cdcd78a9433aa57f34f01d2402e16863431b73da507d5b04b5e0e5c79a8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3423967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f452f7f944b813018ac642c5bc091e1eeddb44dec15e05ba8675b2a968355446`

```dockerfile
```

-	Layers:
	-	`sha256:50438ad815c60487c1cc97bc7ac3167a5f3d6e652cc61ee874256a215a3dcf61`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 3.4 MB (3397592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03334d8b227a09a15df71369cd9ebdb94010cad422fec9e4e8c2fc1433cab39`  
		Last Modified: Fri, 14 Nov 2025 19:45:45 GMT  
		Size: 26.4 KB (26375 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:ff7c819bda0fb2640c79b0a3395fa6d5b67583a0838b732e0f37a1a4734dd513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208322385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494917289c9d267774521ac5599f1877801a2d35b5ae0bd97d227319b0f4495`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:59:43 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:59:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:43 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:59:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:59:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:16:37 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:16:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:16:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7f10bb4cab8241af39f5b5501c8521bff142a1639261b864dbaa26ba4f09b`  
		Last Modified: Wed, 29 Oct 2025 15:09:40 GMT  
		Size: 51.3 MB (51277073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795662ff4ed414582c3847700e3924c8c3e1f69383c1653dc45ff97289c6cdf5`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b641bc33f5a4d376a58cad5e8c1208009b85a6b638bc14778a202d5cbfbb22e0`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f73c281c8872be3944999754ac882be0234869c06ee089c16dde2b3ad94ebff`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 838.6 KB (838589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed47e17a17bcdaf0bd27a90b50ae37de58890bffad0c6502f64060b987cf750`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034be3ec0f654b3d0dbbb6aa9e92342c7cf9da326ab3f711f742e4d3dd0e336e`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 11.7 MB (11666496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975b7e8d29d8073e4f5aa72b21fd3c4ec30d6ec4ddbc09dc5f78060a11c2847`  
		Last Modified: Fri, 14 Nov 2025 19:46:24 GMT  
		Size: 138.3 MB (138264205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6207d62a7c87c88a54029cd54e92e9c31b478e57c63f35be6d1d50ed80cc91f`  
		Last Modified: Fri, 14 Nov 2025 17:20:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:6cf6f1005beec6cead8a33c5dc26ff233af69871f176b2e63bb9dd85c2a378d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141b7670455774617d465d1d7be115f9d349b19a7c95da53541bfc8b786ca1b3`

```dockerfile
```

-	Layers:
	-	`sha256:7e209584134b5a69b318a39c75a7bcb00f09b05034e0a2b51f4359118275b454`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 3.4 MB (3397748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ef1e4256639b8bcb2d7accdbc703d7fa2c0137bb4de694d06799f6135d64cf`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.6 KB (26573 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine3.22`

```console
$ docker pull ghost@sha256:b336036a044d6e0f38427725ce777555ca05bcbefa9d51761c962edcf91242f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine3.22` - linux; amd64

```console
$ docker pull ghost@sha256:e20b75ba2535eb71b1f05f87b00d526b2832c5dca8ae9fac2b06255b8fcb0110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197462745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac976d839b348c5f7aabae4bb681c0febefa62da0eb864d526b44d77adffc28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:16:03 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:16:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:03 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:16:06 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:16:06 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:17:09 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:17:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2cca81d0de31536e59c1e347c529041866e5f6e73effbcd570f0373d4fbaf7`  
		Last Modified: Wed, 29 Oct 2025 14:16:30 GMT  
		Size: 51.6 MB (51567005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1acb8d81a6ae3f5871ce734e5b9aabd5cdb01ccb4fe07ec71c33d75bb4eb04c`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 1.3 MB (1260587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff8b913658cef54b13151d83455a1387472901b28d1f6a0adc49beb04b26ddc`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93780dcece6a389ee0fc2878ac73de722b82d44e5236349ad8019e4f57740dca`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 777.0 KB (777046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb03a2b21b7dd47b4be8e6dc3389204c91156dacd3f6a797875e0665097340`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 923.4 KB (923436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305212959a3c0bcac2d57cf3c9fa68eab4685f0849724388c08c54074e887411`  
		Last Modified: Fri, 14 Nov 2025 17:20:13 GMT  
		Size: 11.7 MB (11661070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f1d5752b1a9e4b15a37f485ed95d8e815fd7560631d635d94bc1870b8c024d`  
		Last Modified: Fri, 14 Nov 2025 17:20:23 GMT  
		Size: 127.5 MB (127470132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59a81117abbc6765eba809e22fab73ba2bf0a860700d424f912640757b34968`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:c40cdcd78a9433aa57f34f01d2402e16863431b73da507d5b04b5e0e5c79a8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3423967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f452f7f944b813018ac642c5bc091e1eeddb44dec15e05ba8675b2a968355446`

```dockerfile
```

-	Layers:
	-	`sha256:50438ad815c60487c1cc97bc7ac3167a5f3d6e652cc61ee874256a215a3dcf61`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 3.4 MB (3397592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03334d8b227a09a15df71369cd9ebdb94010cad422fec9e4e8c2fc1433cab39`  
		Last Modified: Fri, 14 Nov 2025 19:45:45 GMT  
		Size: 26.4 KB (26375 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:ff7c819bda0fb2640c79b0a3395fa6d5b67583a0838b732e0f37a1a4734dd513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208322385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494917289c9d267774521ac5599f1877801a2d35b5ae0bd97d227319b0f4495`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:59:43 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:59:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:43 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:59:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:59:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:16:37 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:16:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:16:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7f10bb4cab8241af39f5b5501c8521bff142a1639261b864dbaa26ba4f09b`  
		Last Modified: Wed, 29 Oct 2025 15:09:40 GMT  
		Size: 51.3 MB (51277073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795662ff4ed414582c3847700e3924c8c3e1f69383c1653dc45ff97289c6cdf5`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b641bc33f5a4d376a58cad5e8c1208009b85a6b638bc14778a202d5cbfbb22e0`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f73c281c8872be3944999754ac882be0234869c06ee089c16dde2b3ad94ebff`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 838.6 KB (838589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed47e17a17bcdaf0bd27a90b50ae37de58890bffad0c6502f64060b987cf750`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034be3ec0f654b3d0dbbb6aa9e92342c7cf9da326ab3f711f742e4d3dd0e336e`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 11.7 MB (11666496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975b7e8d29d8073e4f5aa72b21fd3c4ec30d6ec4ddbc09dc5f78060a11c2847`  
		Last Modified: Fri, 14 Nov 2025 19:46:24 GMT  
		Size: 138.3 MB (138264205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6207d62a7c87c88a54029cd54e92e9c31b478e57c63f35be6d1d50ed80cc91f`  
		Last Modified: Fri, 14 Nov 2025 17:20:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:6cf6f1005beec6cead8a33c5dc26ff233af69871f176b2e63bb9dd85c2a378d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141b7670455774617d465d1d7be115f9d349b19a7c95da53541bfc8b786ca1b3`

```dockerfile
```

-	Layers:
	-	`sha256:7e209584134b5a69b318a39c75a7bcb00f09b05034e0a2b51f4359118275b454`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 3.4 MB (3397748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ef1e4256639b8bcb2d7accdbc703d7fa2c0137bb4de694d06799f6135d64cf`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.6 KB (26573 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-bookworm`

```console
$ docker pull ghost@sha256:85e15524ac7e437720fa4ac3cd4633daaae3f95786a25633415d8d4f7382b4c4
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
$ docker pull ghost@sha256:d6305ad973dec2adb1e34dc71e2306e677e9ae485826162435740e12138b353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220013893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0657b74d11a9a245eda88cdd14a1a2af921eb72358fa1f1d0e7474032933fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:34:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:34:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:37 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:15:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:15:05 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:09 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:09 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427deb858cffe936256f73e134a5baf1b4a26a93b79e03850d2243f6bc1fb302`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d65a4ff088ddf61684b1496e527c5c3accd5af20974f6dd6c3bc58a93412dc`  
		Last Modified: Tue, 04 Nov 2025 00:35:04 GMT  
		Size: 49.5 MB (49481524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6653fee0b024a9e265d5b1d360a35e40e56d7b2212c51acbf76e66c88af4e02`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 1.7 MB (1712601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b7c6f7614440681a3a5b71d3914a7eb7f5122582683ae69e336cd32f238a04`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30f248c587c9e58ca2ee47211c48b240ad9159d324a31e252758ff18b68f77`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 1.2 MB (1247558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44211e7148bae27b3894b362a850d7dd095fdafa9dbea2175f94f7a7c15ce16a`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 11.7 MB (11661069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d95e3f22588236ed74154b6d0a33a31eec2d368e9bf05f8d032fca21638741`  
		Last Modified: Fri, 14 Nov 2025 17:18:22 GMT  
		Size: 127.7 MB (127678242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77aecbe65670514cc189a958e46c069c5bfbf80f12976df53de71d4d0513f8e`  
		Last Modified: Fri, 14 Nov 2025 17:18:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:c9996812fd0e5f37e9e2b5d4bd78dec441a03998d6c7100ae32c1daea95cb9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ac2c21a42e31f5bb89ef9098d4858bf42da1e90c4699c1703c011bf04abce5`

```dockerfile
```

-	Layers:
	-	`sha256:411dbbbb7b2789695a3de35dc7167e3c3a9eaa2b74d7cb01ed3765fc5f2d0bbb`  
		Last Modified: Fri, 14 Nov 2025 19:45:37 GMT  
		Size: 5.6 MB (5610690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f4880ee6e04ecce1050ea974cb0796306623dfc25b6c84f155486f5f2aae4d`  
		Last Modified: Fri, 14 Nov 2025 19:45:38 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:6fb588205dea09931300802a570cafedb86a09af55a54c3d750c34a2b90cede7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211470991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b993d5a857428e277dd35f395d4c38e1d228abefb335b477aa9ff18cdcd8f5a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:45:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:45:27 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:45:40 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:45:40 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:13:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:13:35 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:48 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:49 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:49 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4e79d7f6a82ac834b2b909c91adf66e2efc1389b7e127d8b803cd2a3f7c095`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce593c94118d14798314e3d79e0dfbe9a2a25e8fb36f3d425e2ac3f0aac86b80`  
		Last Modified: Tue, 04 Nov 2025 00:46:06 GMT  
		Size: 44.2 MB (44208200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6316a5dddcba87433a3ac4218d745b63913b646e0d8e387ce926ce0088397de5`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 1.7 MB (1712839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832c6ea2913823d440451db9e0d70234cfb8cd353410b97f145c0fb0a102c2d6`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9751750267a6b953a3de587887881044849607b480b85b892f2d5ab40d6181`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 1.2 MB (1214409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f797f5f0b4bb007779916de8ee6d37f7f5869bd2ace21c9e163299a6c84f4037`  
		Last Modified: Fri, 14 Nov 2025 17:17:50 GMT  
		Size: 11.7 MB (11660119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db2a424c497982a7352c6bd346313619705728b03b78e2e6363e76f063ff134`  
		Last Modified: Fri, 14 Nov 2025 20:23:39 GMT  
		Size: 128.7 MB (128736966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad36ca1c9c94347ef2e30f86a8a83344aac769110da5d73334406f3e67d3f18`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:68ae07f1cddb025b203c7329731967c2376f075be3f4506dd4c64d6882201c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd78e61405dd7e6c2f94c2cc81bec597f4756c28054a64ea6219ebfe84d1616`

```dockerfile
```

-	Layers:
	-	`sha256:37c3534eccf25aa343a7c345cd9ed2999640c0d231082055410e5e084cafd22f`  
		Last Modified: Fri, 14 Nov 2025 19:45:43 GMT  
		Size: 5.6 MB (5613489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e62a0ec9c3265208738ffd9a496a6ddd90aef3e2db9e96d344dc51c15b6e875`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 26.5 KB (26472 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:8d6f3599b40431c17606f590240838ffa35effe0109f502d2543b5c835346784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220075003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb2d4a30d3be8fb6084ffbdefd94aab83b46cf63d4ab0e0ff3e79e563436612`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:35:35 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:35:46 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:35:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:48 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:27 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce654a657d29e2be7faa623cc5a1877b6a78e8b6669ef6e9e48a54b261f2dbb1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36115b3c0ec4b3e7a273bca9f36591f9b2db12432bf4f70ad0f38fee26d12353`  
		Last Modified: Tue, 04 Nov 2025 00:36:13 GMT  
		Size: 49.6 MB (49614672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53479a8a7fd9dfad5cc88f68b7182c993f5e24b6cfc0b672e3c96b28eadc3da9`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be8e8db985232f1716a04e833933730acd9419ec49aa51c1f1aa69fe22888e1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29f9b4dcd7e856a096ca07550a76b23003c52689d12394cb194daf637fd35e8`  
		Last Modified: Fri, 14 Nov 2025 17:18:45 GMT  
		Size: 1.2 MB (1201445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e917f52639864038fbd445a1047ab571f36715192e655b1d5e33925a16354f`  
		Last Modified: Fri, 14 Nov 2025 17:18:46 GMT  
		Size: 11.7 MB (11666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567d8828b01841392dcf0dec341fe287fbf97ce1e1929e6e32dd8695d51b257d`  
		Last Modified: Fri, 14 Nov 2025 17:19:04 GMT  
		Size: 127.8 MB (127772964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3222ac9c7fc4d2dd2ab35916c7a28642609a55b223c5157379fb85bc15a2cebd`  
		Last Modified: Fri, 14 Nov 2025 17:18:44 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:56215ea56599da1bac73faf28a96259dc0479ae63a86ff364bbd90dcc7724e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6adac70a75f2b20757743143591caa6e38377ba58f3a19bc2720bc0c8de3073`

```dockerfile
```

-	Layers:
	-	`sha256:d1a67ed51384953de0b80812877aeafa3ab4d77d73b8d3a65a991d1c6567d6fa`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 5.6 MB (5611041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2e739425d1eef4534729048ffb99a1cfef0b1f96ea1ce2b896b9694bc38cbc5`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.5 KB (26516 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:cfd3d21d5e1501f362a50c090a0dfebfdbdbfb6a5251c68cc7866c581447b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221995814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483f844dc2b67fe79f4cc732a0b6547572e68c3e37e1660755d293490e38fa75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:33:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 03:35:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 03:35:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:35:48 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:21 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:39 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:43 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:43 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:43 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:44 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b483b0df66cd8c70ba210c61fdc3840348da24bad86177f3799a15a254e527`  
		Last Modified: Tue, 04 Nov 2025 03:34:01 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b320a6187066ba76389a7c79a1ddcb01d2b7798c2b10f4a370838218e2b7502`  
		Last Modified: Tue, 04 Nov 2025 03:36:30 GMT  
		Size: 49.7 MB (49676869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94b7e8c1441d6d3f81305d6be716fd246c56e2ffe42813414eee448bcc0db3d`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b080f614a4846400e9341eea05bfc895791733a0574b3b7a0e133f7095e26c3b`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e25b4aea4e283179ce72acb52f272e26fdc644f71a2f31d91ce19c7cb83c9a4`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 1.2 MB (1221305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b5b430011654539652162ae126fad71141236f36f4bd289668bffd636e4597`  
		Last Modified: Fri, 14 Nov 2025 17:17:56 GMT  
		Size: 11.7 MB (11676181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffba5d1b26178851461a6d7112f84646693457b752e5ee763672efed2aaa2013`  
		Last Modified: Fri, 14 Nov 2025 17:17:37 GMT  
		Size: 130.8 MB (130819971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1617d5b92e47b9096b44c75075adef4bb47445928af5b155ae01683c2375062d`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:00547a5deba99ed2a3feaf2c865feeb31da0b741f8dad07caae3b66249f9725b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c118fdb5d65f98f9c554f78161e9cd1326cbbbbbba84d9a10d93e9a76b1a48d6`

```dockerfile
```

-	Layers:
	-	`sha256:62eab9ad244f580d8fcab14bd3eccf3e0196228bd3ccac84cf7b891b8c28b586`  
		Last Modified: Fri, 14 Nov 2025 19:45:55 GMT  
		Size: 5.6 MB (5604517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc702032869af479006fa83b52bb022c5877562d2508f26b9380b61b2e3264`  
		Last Modified: Fri, 14 Nov 2025 19:45:56 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.8`

```console
$ docker pull ghost@sha256:85e15524ac7e437720fa4ac3cd4633daaae3f95786a25633415d8d4f7382b4c4
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

### `ghost:6.8` - linux; amd64

```console
$ docker pull ghost@sha256:d6305ad973dec2adb1e34dc71e2306e677e9ae485826162435740e12138b353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220013893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0657b74d11a9a245eda88cdd14a1a2af921eb72358fa1f1d0e7474032933fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:34:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:34:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:37 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:15:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:15:05 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:09 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:09 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427deb858cffe936256f73e134a5baf1b4a26a93b79e03850d2243f6bc1fb302`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d65a4ff088ddf61684b1496e527c5c3accd5af20974f6dd6c3bc58a93412dc`  
		Last Modified: Tue, 04 Nov 2025 00:35:04 GMT  
		Size: 49.5 MB (49481524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6653fee0b024a9e265d5b1d360a35e40e56d7b2212c51acbf76e66c88af4e02`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 1.7 MB (1712601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b7c6f7614440681a3a5b71d3914a7eb7f5122582683ae69e336cd32f238a04`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30f248c587c9e58ca2ee47211c48b240ad9159d324a31e252758ff18b68f77`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 1.2 MB (1247558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44211e7148bae27b3894b362a850d7dd095fdafa9dbea2175f94f7a7c15ce16a`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 11.7 MB (11661069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d95e3f22588236ed74154b6d0a33a31eec2d368e9bf05f8d032fca21638741`  
		Last Modified: Fri, 14 Nov 2025 17:18:22 GMT  
		Size: 127.7 MB (127678242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77aecbe65670514cc189a958e46c069c5bfbf80f12976df53de71d4d0513f8e`  
		Last Modified: Fri, 14 Nov 2025 17:18:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8` - unknown; unknown

```console
$ docker pull ghost@sha256:c9996812fd0e5f37e9e2b5d4bd78dec441a03998d6c7100ae32c1daea95cb9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ac2c21a42e31f5bb89ef9098d4858bf42da1e90c4699c1703c011bf04abce5`

```dockerfile
```

-	Layers:
	-	`sha256:411dbbbb7b2789695a3de35dc7167e3c3a9eaa2b74d7cb01ed3765fc5f2d0bbb`  
		Last Modified: Fri, 14 Nov 2025 19:45:37 GMT  
		Size: 5.6 MB (5610690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f4880ee6e04ecce1050ea974cb0796306623dfc25b6c84f155486f5f2aae4d`  
		Last Modified: Fri, 14 Nov 2025 19:45:38 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8` - linux; arm variant v7

```console
$ docker pull ghost@sha256:6fb588205dea09931300802a570cafedb86a09af55a54c3d750c34a2b90cede7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211470991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b993d5a857428e277dd35f395d4c38e1d228abefb335b477aa9ff18cdcd8f5a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:45:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:45:27 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:45:40 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:45:40 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:13:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:13:35 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:48 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:49 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:49 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4e79d7f6a82ac834b2b909c91adf66e2efc1389b7e127d8b803cd2a3f7c095`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce593c94118d14798314e3d79e0dfbe9a2a25e8fb36f3d425e2ac3f0aac86b80`  
		Last Modified: Tue, 04 Nov 2025 00:46:06 GMT  
		Size: 44.2 MB (44208200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6316a5dddcba87433a3ac4218d745b63913b646e0d8e387ce926ce0088397de5`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 1.7 MB (1712839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832c6ea2913823d440451db9e0d70234cfb8cd353410b97f145c0fb0a102c2d6`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9751750267a6b953a3de587887881044849607b480b85b892f2d5ab40d6181`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 1.2 MB (1214409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f797f5f0b4bb007779916de8ee6d37f7f5869bd2ace21c9e163299a6c84f4037`  
		Last Modified: Fri, 14 Nov 2025 17:17:50 GMT  
		Size: 11.7 MB (11660119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db2a424c497982a7352c6bd346313619705728b03b78e2e6363e76f063ff134`  
		Last Modified: Fri, 14 Nov 2025 20:23:39 GMT  
		Size: 128.7 MB (128736966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad36ca1c9c94347ef2e30f86a8a83344aac769110da5d73334406f3e67d3f18`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8` - unknown; unknown

```console
$ docker pull ghost@sha256:68ae07f1cddb025b203c7329731967c2376f075be3f4506dd4c64d6882201c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd78e61405dd7e6c2f94c2cc81bec597f4756c28054a64ea6219ebfe84d1616`

```dockerfile
```

-	Layers:
	-	`sha256:37c3534eccf25aa343a7c345cd9ed2999640c0d231082055410e5e084cafd22f`  
		Last Modified: Fri, 14 Nov 2025 19:45:43 GMT  
		Size: 5.6 MB (5613489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e62a0ec9c3265208738ffd9a496a6ddd90aef3e2db9e96d344dc51c15b6e875`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 26.5 KB (26472 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:8d6f3599b40431c17606f590240838ffa35effe0109f502d2543b5c835346784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220075003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb2d4a30d3be8fb6084ffbdefd94aab83b46cf63d4ab0e0ff3e79e563436612`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:35:35 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:35:46 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:35:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:48 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:27 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce654a657d29e2be7faa623cc5a1877b6a78e8b6669ef6e9e48a54b261f2dbb1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36115b3c0ec4b3e7a273bca9f36591f9b2db12432bf4f70ad0f38fee26d12353`  
		Last Modified: Tue, 04 Nov 2025 00:36:13 GMT  
		Size: 49.6 MB (49614672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53479a8a7fd9dfad5cc88f68b7182c993f5e24b6cfc0b672e3c96b28eadc3da9`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be8e8db985232f1716a04e833933730acd9419ec49aa51c1f1aa69fe22888e1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29f9b4dcd7e856a096ca07550a76b23003c52689d12394cb194daf637fd35e8`  
		Last Modified: Fri, 14 Nov 2025 17:18:45 GMT  
		Size: 1.2 MB (1201445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e917f52639864038fbd445a1047ab571f36715192e655b1d5e33925a16354f`  
		Last Modified: Fri, 14 Nov 2025 17:18:46 GMT  
		Size: 11.7 MB (11666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567d8828b01841392dcf0dec341fe287fbf97ce1e1929e6e32dd8695d51b257d`  
		Last Modified: Fri, 14 Nov 2025 17:19:04 GMT  
		Size: 127.8 MB (127772964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3222ac9c7fc4d2dd2ab35916c7a28642609a55b223c5157379fb85bc15a2cebd`  
		Last Modified: Fri, 14 Nov 2025 17:18:44 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8` - unknown; unknown

```console
$ docker pull ghost@sha256:56215ea56599da1bac73faf28a96259dc0479ae63a86ff364bbd90dcc7724e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6adac70a75f2b20757743143591caa6e38377ba58f3a19bc2720bc0c8de3073`

```dockerfile
```

-	Layers:
	-	`sha256:d1a67ed51384953de0b80812877aeafa3ab4d77d73b8d3a65a991d1c6567d6fa`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 5.6 MB (5611041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2e739425d1eef4534729048ffb99a1cfef0b1f96ea1ce2b896b9694bc38cbc5`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.5 KB (26516 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8` - linux; s390x

```console
$ docker pull ghost@sha256:cfd3d21d5e1501f362a50c090a0dfebfdbdbfb6a5251c68cc7866c581447b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221995814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483f844dc2b67fe79f4cc732a0b6547572e68c3e37e1660755d293490e38fa75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:33:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 03:35:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 03:35:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:35:48 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:21 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:39 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:43 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:43 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:43 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:44 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b483b0df66cd8c70ba210c61fdc3840348da24bad86177f3799a15a254e527`  
		Last Modified: Tue, 04 Nov 2025 03:34:01 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b320a6187066ba76389a7c79a1ddcb01d2b7798c2b10f4a370838218e2b7502`  
		Last Modified: Tue, 04 Nov 2025 03:36:30 GMT  
		Size: 49.7 MB (49676869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94b7e8c1441d6d3f81305d6be716fd246c56e2ffe42813414eee448bcc0db3d`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b080f614a4846400e9341eea05bfc895791733a0574b3b7a0e133f7095e26c3b`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e25b4aea4e283179ce72acb52f272e26fdc644f71a2f31d91ce19c7cb83c9a4`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 1.2 MB (1221305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b5b430011654539652162ae126fad71141236f36f4bd289668bffd636e4597`  
		Last Modified: Fri, 14 Nov 2025 17:17:56 GMT  
		Size: 11.7 MB (11676181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffba5d1b26178851461a6d7112f84646693457b752e5ee763672efed2aaa2013`  
		Last Modified: Fri, 14 Nov 2025 17:17:37 GMT  
		Size: 130.8 MB (130819971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1617d5b92e47b9096b44c75075adef4bb47445928af5b155ae01683c2375062d`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8` - unknown; unknown

```console
$ docker pull ghost@sha256:00547a5deba99ed2a3feaf2c865feeb31da0b741f8dad07caae3b66249f9725b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c118fdb5d65f98f9c554f78161e9cd1326cbbbbbba84d9a10d93e9a76b1a48d6`

```dockerfile
```

-	Layers:
	-	`sha256:62eab9ad244f580d8fcab14bd3eccf3e0196228bd3ccac84cf7b891b8c28b586`  
		Last Modified: Fri, 14 Nov 2025 19:45:55 GMT  
		Size: 5.6 MB (5604517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc702032869af479006fa83b52bb022c5877562d2508f26b9380b61b2e3264`  
		Last Modified: Fri, 14 Nov 2025 19:45:56 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.8-alpine`

```console
$ docker pull ghost@sha256:b336036a044d6e0f38427725ce777555ca05bcbefa9d51761c962edcf91242f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.8-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:e20b75ba2535eb71b1f05f87b00d526b2832c5dca8ae9fac2b06255b8fcb0110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197462745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac976d839b348c5f7aabae4bb681c0febefa62da0eb864d526b44d77adffc28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:16:03 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:16:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:03 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:16:06 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:16:06 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:17:09 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:17:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2cca81d0de31536e59c1e347c529041866e5f6e73effbcd570f0373d4fbaf7`  
		Last Modified: Wed, 29 Oct 2025 14:16:30 GMT  
		Size: 51.6 MB (51567005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1acb8d81a6ae3f5871ce734e5b9aabd5cdb01ccb4fe07ec71c33d75bb4eb04c`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 1.3 MB (1260587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff8b913658cef54b13151d83455a1387472901b28d1f6a0adc49beb04b26ddc`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93780dcece6a389ee0fc2878ac73de722b82d44e5236349ad8019e4f57740dca`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 777.0 KB (777046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb03a2b21b7dd47b4be8e6dc3389204c91156dacd3f6a797875e0665097340`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 923.4 KB (923436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305212959a3c0bcac2d57cf3c9fa68eab4685f0849724388c08c54074e887411`  
		Last Modified: Fri, 14 Nov 2025 17:20:13 GMT  
		Size: 11.7 MB (11661070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f1d5752b1a9e4b15a37f485ed95d8e815fd7560631d635d94bc1870b8c024d`  
		Last Modified: Fri, 14 Nov 2025 17:20:23 GMT  
		Size: 127.5 MB (127470132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59a81117abbc6765eba809e22fab73ba2bf0a860700d424f912640757b34968`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c40cdcd78a9433aa57f34f01d2402e16863431b73da507d5b04b5e0e5c79a8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3423967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f452f7f944b813018ac642c5bc091e1eeddb44dec15e05ba8675b2a968355446`

```dockerfile
```

-	Layers:
	-	`sha256:50438ad815c60487c1cc97bc7ac3167a5f3d6e652cc61ee874256a215a3dcf61`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 3.4 MB (3397592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03334d8b227a09a15df71369cd9ebdb94010cad422fec9e4e8c2fc1433cab39`  
		Last Modified: Fri, 14 Nov 2025 19:45:45 GMT  
		Size: 26.4 KB (26375 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:ff7c819bda0fb2640c79b0a3395fa6d5b67583a0838b732e0f37a1a4734dd513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208322385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494917289c9d267774521ac5599f1877801a2d35b5ae0bd97d227319b0f4495`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:59:43 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:59:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:43 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:59:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:59:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:16:37 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:16:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:16:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7f10bb4cab8241af39f5b5501c8521bff142a1639261b864dbaa26ba4f09b`  
		Last Modified: Wed, 29 Oct 2025 15:09:40 GMT  
		Size: 51.3 MB (51277073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795662ff4ed414582c3847700e3924c8c3e1f69383c1653dc45ff97289c6cdf5`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b641bc33f5a4d376a58cad5e8c1208009b85a6b638bc14778a202d5cbfbb22e0`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f73c281c8872be3944999754ac882be0234869c06ee089c16dde2b3ad94ebff`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 838.6 KB (838589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed47e17a17bcdaf0bd27a90b50ae37de58890bffad0c6502f64060b987cf750`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034be3ec0f654b3d0dbbb6aa9e92342c7cf9da326ab3f711f742e4d3dd0e336e`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 11.7 MB (11666496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975b7e8d29d8073e4f5aa72b21fd3c4ec30d6ec4ddbc09dc5f78060a11c2847`  
		Last Modified: Fri, 14 Nov 2025 19:46:24 GMT  
		Size: 138.3 MB (138264205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6207d62a7c87c88a54029cd54e92e9c31b478e57c63f35be6d1d50ed80cc91f`  
		Last Modified: Fri, 14 Nov 2025 17:20:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:6cf6f1005beec6cead8a33c5dc26ff233af69871f176b2e63bb9dd85c2a378d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141b7670455774617d465d1d7be115f9d349b19a7c95da53541bfc8b786ca1b3`

```dockerfile
```

-	Layers:
	-	`sha256:7e209584134b5a69b318a39c75a7bcb00f09b05034e0a2b51f4359118275b454`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 3.4 MB (3397748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ef1e4256639b8bcb2d7accdbc703d7fa2c0137bb4de694d06799f6135d64cf`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.6 KB (26573 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.8-alpine3.22`

```console
$ docker pull ghost@sha256:b336036a044d6e0f38427725ce777555ca05bcbefa9d51761c962edcf91242f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.8-alpine3.22` - linux; amd64

```console
$ docker pull ghost@sha256:e20b75ba2535eb71b1f05f87b00d526b2832c5dca8ae9fac2b06255b8fcb0110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197462745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac976d839b348c5f7aabae4bb681c0febefa62da0eb864d526b44d77adffc28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:16:03 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:16:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:03 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:16:06 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:16:06 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:17:09 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:17:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2cca81d0de31536e59c1e347c529041866e5f6e73effbcd570f0373d4fbaf7`  
		Last Modified: Wed, 29 Oct 2025 14:16:30 GMT  
		Size: 51.6 MB (51567005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1acb8d81a6ae3f5871ce734e5b9aabd5cdb01ccb4fe07ec71c33d75bb4eb04c`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 1.3 MB (1260587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff8b913658cef54b13151d83455a1387472901b28d1f6a0adc49beb04b26ddc`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93780dcece6a389ee0fc2878ac73de722b82d44e5236349ad8019e4f57740dca`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 777.0 KB (777046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb03a2b21b7dd47b4be8e6dc3389204c91156dacd3f6a797875e0665097340`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 923.4 KB (923436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305212959a3c0bcac2d57cf3c9fa68eab4685f0849724388c08c54074e887411`  
		Last Modified: Fri, 14 Nov 2025 17:20:13 GMT  
		Size: 11.7 MB (11661070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f1d5752b1a9e4b15a37f485ed95d8e815fd7560631d635d94bc1870b8c024d`  
		Last Modified: Fri, 14 Nov 2025 17:20:23 GMT  
		Size: 127.5 MB (127470132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59a81117abbc6765eba809e22fab73ba2bf0a860700d424f912640757b34968`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:c40cdcd78a9433aa57f34f01d2402e16863431b73da507d5b04b5e0e5c79a8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3423967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f452f7f944b813018ac642c5bc091e1eeddb44dec15e05ba8675b2a968355446`

```dockerfile
```

-	Layers:
	-	`sha256:50438ad815c60487c1cc97bc7ac3167a5f3d6e652cc61ee874256a215a3dcf61`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 3.4 MB (3397592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03334d8b227a09a15df71369cd9ebdb94010cad422fec9e4e8c2fc1433cab39`  
		Last Modified: Fri, 14 Nov 2025 19:45:45 GMT  
		Size: 26.4 KB (26375 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:ff7c819bda0fb2640c79b0a3395fa6d5b67583a0838b732e0f37a1a4734dd513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208322385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494917289c9d267774521ac5599f1877801a2d35b5ae0bd97d227319b0f4495`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:59:43 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:59:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:43 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:59:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:59:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:16:37 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:16:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:16:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7f10bb4cab8241af39f5b5501c8521bff142a1639261b864dbaa26ba4f09b`  
		Last Modified: Wed, 29 Oct 2025 15:09:40 GMT  
		Size: 51.3 MB (51277073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795662ff4ed414582c3847700e3924c8c3e1f69383c1653dc45ff97289c6cdf5`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b641bc33f5a4d376a58cad5e8c1208009b85a6b638bc14778a202d5cbfbb22e0`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f73c281c8872be3944999754ac882be0234869c06ee089c16dde2b3ad94ebff`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 838.6 KB (838589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed47e17a17bcdaf0bd27a90b50ae37de58890bffad0c6502f64060b987cf750`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034be3ec0f654b3d0dbbb6aa9e92342c7cf9da326ab3f711f742e4d3dd0e336e`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 11.7 MB (11666496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975b7e8d29d8073e4f5aa72b21fd3c4ec30d6ec4ddbc09dc5f78060a11c2847`  
		Last Modified: Fri, 14 Nov 2025 19:46:24 GMT  
		Size: 138.3 MB (138264205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6207d62a7c87c88a54029cd54e92e9c31b478e57c63f35be6d1d50ed80cc91f`  
		Last Modified: Fri, 14 Nov 2025 17:20:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:6cf6f1005beec6cead8a33c5dc26ff233af69871f176b2e63bb9dd85c2a378d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141b7670455774617d465d1d7be115f9d349b19a7c95da53541bfc8b786ca1b3`

```dockerfile
```

-	Layers:
	-	`sha256:7e209584134b5a69b318a39c75a7bcb00f09b05034e0a2b51f4359118275b454`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 3.4 MB (3397748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ef1e4256639b8bcb2d7accdbc703d7fa2c0137bb4de694d06799f6135d64cf`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.6 KB (26573 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.8-bookworm`

```console
$ docker pull ghost@sha256:85e15524ac7e437720fa4ac3cd4633daaae3f95786a25633415d8d4f7382b4c4
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

### `ghost:6.8-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:d6305ad973dec2adb1e34dc71e2306e677e9ae485826162435740e12138b353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220013893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0657b74d11a9a245eda88cdd14a1a2af921eb72358fa1f1d0e7474032933fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:34:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:34:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:37 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:15:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:15:05 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:09 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:09 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427deb858cffe936256f73e134a5baf1b4a26a93b79e03850d2243f6bc1fb302`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d65a4ff088ddf61684b1496e527c5c3accd5af20974f6dd6c3bc58a93412dc`  
		Last Modified: Tue, 04 Nov 2025 00:35:04 GMT  
		Size: 49.5 MB (49481524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6653fee0b024a9e265d5b1d360a35e40e56d7b2212c51acbf76e66c88af4e02`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 1.7 MB (1712601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b7c6f7614440681a3a5b71d3914a7eb7f5122582683ae69e336cd32f238a04`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30f248c587c9e58ca2ee47211c48b240ad9159d324a31e252758ff18b68f77`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 1.2 MB (1247558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44211e7148bae27b3894b362a850d7dd095fdafa9dbea2175f94f7a7c15ce16a`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 11.7 MB (11661069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d95e3f22588236ed74154b6d0a33a31eec2d368e9bf05f8d032fca21638741`  
		Last Modified: Fri, 14 Nov 2025 17:18:22 GMT  
		Size: 127.7 MB (127678242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77aecbe65670514cc189a958e46c069c5bfbf80f12976df53de71d4d0513f8e`  
		Last Modified: Fri, 14 Nov 2025 17:18:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:c9996812fd0e5f37e9e2b5d4bd78dec441a03998d6c7100ae32c1daea95cb9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ac2c21a42e31f5bb89ef9098d4858bf42da1e90c4699c1703c011bf04abce5`

```dockerfile
```

-	Layers:
	-	`sha256:411dbbbb7b2789695a3de35dc7167e3c3a9eaa2b74d7cb01ed3765fc5f2d0bbb`  
		Last Modified: Fri, 14 Nov 2025 19:45:37 GMT  
		Size: 5.6 MB (5610690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f4880ee6e04ecce1050ea974cb0796306623dfc25b6c84f155486f5f2aae4d`  
		Last Modified: Fri, 14 Nov 2025 19:45:38 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:6fb588205dea09931300802a570cafedb86a09af55a54c3d750c34a2b90cede7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211470991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b993d5a857428e277dd35f395d4c38e1d228abefb335b477aa9ff18cdcd8f5a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:45:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:45:27 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:45:40 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:45:40 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:13:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:13:35 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:48 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:49 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:49 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4e79d7f6a82ac834b2b909c91adf66e2efc1389b7e127d8b803cd2a3f7c095`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce593c94118d14798314e3d79e0dfbe9a2a25e8fb36f3d425e2ac3f0aac86b80`  
		Last Modified: Tue, 04 Nov 2025 00:46:06 GMT  
		Size: 44.2 MB (44208200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6316a5dddcba87433a3ac4218d745b63913b646e0d8e387ce926ce0088397de5`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 1.7 MB (1712839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832c6ea2913823d440451db9e0d70234cfb8cd353410b97f145c0fb0a102c2d6`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9751750267a6b953a3de587887881044849607b480b85b892f2d5ab40d6181`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 1.2 MB (1214409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f797f5f0b4bb007779916de8ee6d37f7f5869bd2ace21c9e163299a6c84f4037`  
		Last Modified: Fri, 14 Nov 2025 17:17:50 GMT  
		Size: 11.7 MB (11660119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db2a424c497982a7352c6bd346313619705728b03b78e2e6363e76f063ff134`  
		Last Modified: Fri, 14 Nov 2025 20:23:39 GMT  
		Size: 128.7 MB (128736966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad36ca1c9c94347ef2e30f86a8a83344aac769110da5d73334406f3e67d3f18`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:68ae07f1cddb025b203c7329731967c2376f075be3f4506dd4c64d6882201c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd78e61405dd7e6c2f94c2cc81bec597f4756c28054a64ea6219ebfe84d1616`

```dockerfile
```

-	Layers:
	-	`sha256:37c3534eccf25aa343a7c345cd9ed2999640c0d231082055410e5e084cafd22f`  
		Last Modified: Fri, 14 Nov 2025 19:45:43 GMT  
		Size: 5.6 MB (5613489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e62a0ec9c3265208738ffd9a496a6ddd90aef3e2db9e96d344dc51c15b6e875`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 26.5 KB (26472 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:8d6f3599b40431c17606f590240838ffa35effe0109f502d2543b5c835346784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220075003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb2d4a30d3be8fb6084ffbdefd94aab83b46cf63d4ab0e0ff3e79e563436612`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:35:35 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:35:46 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:35:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:48 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:27 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce654a657d29e2be7faa623cc5a1877b6a78e8b6669ef6e9e48a54b261f2dbb1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36115b3c0ec4b3e7a273bca9f36591f9b2db12432bf4f70ad0f38fee26d12353`  
		Last Modified: Tue, 04 Nov 2025 00:36:13 GMT  
		Size: 49.6 MB (49614672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53479a8a7fd9dfad5cc88f68b7182c993f5e24b6cfc0b672e3c96b28eadc3da9`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be8e8db985232f1716a04e833933730acd9419ec49aa51c1f1aa69fe22888e1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29f9b4dcd7e856a096ca07550a76b23003c52689d12394cb194daf637fd35e8`  
		Last Modified: Fri, 14 Nov 2025 17:18:45 GMT  
		Size: 1.2 MB (1201445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e917f52639864038fbd445a1047ab571f36715192e655b1d5e33925a16354f`  
		Last Modified: Fri, 14 Nov 2025 17:18:46 GMT  
		Size: 11.7 MB (11666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567d8828b01841392dcf0dec341fe287fbf97ce1e1929e6e32dd8695d51b257d`  
		Last Modified: Fri, 14 Nov 2025 17:19:04 GMT  
		Size: 127.8 MB (127772964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3222ac9c7fc4d2dd2ab35916c7a28642609a55b223c5157379fb85bc15a2cebd`  
		Last Modified: Fri, 14 Nov 2025 17:18:44 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:56215ea56599da1bac73faf28a96259dc0479ae63a86ff364bbd90dcc7724e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6adac70a75f2b20757743143591caa6e38377ba58f3a19bc2720bc0c8de3073`

```dockerfile
```

-	Layers:
	-	`sha256:d1a67ed51384953de0b80812877aeafa3ab4d77d73b8d3a65a991d1c6567d6fa`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 5.6 MB (5611041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2e739425d1eef4534729048ffb99a1cfef0b1f96ea1ce2b896b9694bc38cbc5`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.5 KB (26516 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:cfd3d21d5e1501f362a50c090a0dfebfdbdbfb6a5251c68cc7866c581447b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221995814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483f844dc2b67fe79f4cc732a0b6547572e68c3e37e1660755d293490e38fa75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:33:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 03:35:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 03:35:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:35:48 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:21 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:39 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:43 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:43 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:43 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:44 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b483b0df66cd8c70ba210c61fdc3840348da24bad86177f3799a15a254e527`  
		Last Modified: Tue, 04 Nov 2025 03:34:01 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b320a6187066ba76389a7c79a1ddcb01d2b7798c2b10f4a370838218e2b7502`  
		Last Modified: Tue, 04 Nov 2025 03:36:30 GMT  
		Size: 49.7 MB (49676869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94b7e8c1441d6d3f81305d6be716fd246c56e2ffe42813414eee448bcc0db3d`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b080f614a4846400e9341eea05bfc895791733a0574b3b7a0e133f7095e26c3b`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e25b4aea4e283179ce72acb52f272e26fdc644f71a2f31d91ce19c7cb83c9a4`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 1.2 MB (1221305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b5b430011654539652162ae126fad71141236f36f4bd289668bffd636e4597`  
		Last Modified: Fri, 14 Nov 2025 17:17:56 GMT  
		Size: 11.7 MB (11676181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffba5d1b26178851461a6d7112f84646693457b752e5ee763672efed2aaa2013`  
		Last Modified: Fri, 14 Nov 2025 17:17:37 GMT  
		Size: 130.8 MB (130819971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1617d5b92e47b9096b44c75075adef4bb47445928af5b155ae01683c2375062d`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:00547a5deba99ed2a3feaf2c865feeb31da0b741f8dad07caae3b66249f9725b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c118fdb5d65f98f9c554f78161e9cd1326cbbbbbba84d9a10d93e9a76b1a48d6`

```dockerfile
```

-	Layers:
	-	`sha256:62eab9ad244f580d8fcab14bd3eccf3e0196228bd3ccac84cf7b891b8c28b586`  
		Last Modified: Fri, 14 Nov 2025 19:45:55 GMT  
		Size: 5.6 MB (5604517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc702032869af479006fa83b52bb022c5877562d2508f26b9380b61b2e3264`  
		Last Modified: Fri, 14 Nov 2025 19:45:56 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.8.0`

```console
$ docker pull ghost@sha256:85e15524ac7e437720fa4ac3cd4633daaae3f95786a25633415d8d4f7382b4c4
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

### `ghost:6.8.0` - linux; amd64

```console
$ docker pull ghost@sha256:d6305ad973dec2adb1e34dc71e2306e677e9ae485826162435740e12138b353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220013893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0657b74d11a9a245eda88cdd14a1a2af921eb72358fa1f1d0e7474032933fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:34:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:34:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:37 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:15:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:15:05 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:09 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:09 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427deb858cffe936256f73e134a5baf1b4a26a93b79e03850d2243f6bc1fb302`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d65a4ff088ddf61684b1496e527c5c3accd5af20974f6dd6c3bc58a93412dc`  
		Last Modified: Tue, 04 Nov 2025 00:35:04 GMT  
		Size: 49.5 MB (49481524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6653fee0b024a9e265d5b1d360a35e40e56d7b2212c51acbf76e66c88af4e02`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 1.7 MB (1712601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b7c6f7614440681a3a5b71d3914a7eb7f5122582683ae69e336cd32f238a04`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30f248c587c9e58ca2ee47211c48b240ad9159d324a31e252758ff18b68f77`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 1.2 MB (1247558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44211e7148bae27b3894b362a850d7dd095fdafa9dbea2175f94f7a7c15ce16a`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 11.7 MB (11661069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d95e3f22588236ed74154b6d0a33a31eec2d368e9bf05f8d032fca21638741`  
		Last Modified: Fri, 14 Nov 2025 17:18:22 GMT  
		Size: 127.7 MB (127678242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77aecbe65670514cc189a958e46c069c5bfbf80f12976df53de71d4d0513f8e`  
		Last Modified: Fri, 14 Nov 2025 17:18:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8.0` - unknown; unknown

```console
$ docker pull ghost@sha256:c9996812fd0e5f37e9e2b5d4bd78dec441a03998d6c7100ae32c1daea95cb9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ac2c21a42e31f5bb89ef9098d4858bf42da1e90c4699c1703c011bf04abce5`

```dockerfile
```

-	Layers:
	-	`sha256:411dbbbb7b2789695a3de35dc7167e3c3a9eaa2b74d7cb01ed3765fc5f2d0bbb`  
		Last Modified: Fri, 14 Nov 2025 19:45:37 GMT  
		Size: 5.6 MB (5610690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f4880ee6e04ecce1050ea974cb0796306623dfc25b6c84f155486f5f2aae4d`  
		Last Modified: Fri, 14 Nov 2025 19:45:38 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8.0` - linux; arm variant v7

```console
$ docker pull ghost@sha256:6fb588205dea09931300802a570cafedb86a09af55a54c3d750c34a2b90cede7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211470991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b993d5a857428e277dd35f395d4c38e1d228abefb335b477aa9ff18cdcd8f5a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:45:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:45:27 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:45:40 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:45:40 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:13:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:13:35 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:48 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:49 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:49 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4e79d7f6a82ac834b2b909c91adf66e2efc1389b7e127d8b803cd2a3f7c095`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce593c94118d14798314e3d79e0dfbe9a2a25e8fb36f3d425e2ac3f0aac86b80`  
		Last Modified: Tue, 04 Nov 2025 00:46:06 GMT  
		Size: 44.2 MB (44208200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6316a5dddcba87433a3ac4218d745b63913b646e0d8e387ce926ce0088397de5`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 1.7 MB (1712839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832c6ea2913823d440451db9e0d70234cfb8cd353410b97f145c0fb0a102c2d6`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9751750267a6b953a3de587887881044849607b480b85b892f2d5ab40d6181`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 1.2 MB (1214409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f797f5f0b4bb007779916de8ee6d37f7f5869bd2ace21c9e163299a6c84f4037`  
		Last Modified: Fri, 14 Nov 2025 17:17:50 GMT  
		Size: 11.7 MB (11660119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db2a424c497982a7352c6bd346313619705728b03b78e2e6363e76f063ff134`  
		Last Modified: Fri, 14 Nov 2025 20:23:39 GMT  
		Size: 128.7 MB (128736966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad36ca1c9c94347ef2e30f86a8a83344aac769110da5d73334406f3e67d3f18`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8.0` - unknown; unknown

```console
$ docker pull ghost@sha256:68ae07f1cddb025b203c7329731967c2376f075be3f4506dd4c64d6882201c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd78e61405dd7e6c2f94c2cc81bec597f4756c28054a64ea6219ebfe84d1616`

```dockerfile
```

-	Layers:
	-	`sha256:37c3534eccf25aa343a7c345cd9ed2999640c0d231082055410e5e084cafd22f`  
		Last Modified: Fri, 14 Nov 2025 19:45:43 GMT  
		Size: 5.6 MB (5613489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e62a0ec9c3265208738ffd9a496a6ddd90aef3e2db9e96d344dc51c15b6e875`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 26.5 KB (26472 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8.0` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:8d6f3599b40431c17606f590240838ffa35effe0109f502d2543b5c835346784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220075003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb2d4a30d3be8fb6084ffbdefd94aab83b46cf63d4ab0e0ff3e79e563436612`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:35:35 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:35:46 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:35:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:48 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:27 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce654a657d29e2be7faa623cc5a1877b6a78e8b6669ef6e9e48a54b261f2dbb1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36115b3c0ec4b3e7a273bca9f36591f9b2db12432bf4f70ad0f38fee26d12353`  
		Last Modified: Tue, 04 Nov 2025 00:36:13 GMT  
		Size: 49.6 MB (49614672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53479a8a7fd9dfad5cc88f68b7182c993f5e24b6cfc0b672e3c96b28eadc3da9`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be8e8db985232f1716a04e833933730acd9419ec49aa51c1f1aa69fe22888e1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29f9b4dcd7e856a096ca07550a76b23003c52689d12394cb194daf637fd35e8`  
		Last Modified: Fri, 14 Nov 2025 17:18:45 GMT  
		Size: 1.2 MB (1201445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e917f52639864038fbd445a1047ab571f36715192e655b1d5e33925a16354f`  
		Last Modified: Fri, 14 Nov 2025 17:18:46 GMT  
		Size: 11.7 MB (11666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567d8828b01841392dcf0dec341fe287fbf97ce1e1929e6e32dd8695d51b257d`  
		Last Modified: Fri, 14 Nov 2025 17:19:04 GMT  
		Size: 127.8 MB (127772964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3222ac9c7fc4d2dd2ab35916c7a28642609a55b223c5157379fb85bc15a2cebd`  
		Last Modified: Fri, 14 Nov 2025 17:18:44 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8.0` - unknown; unknown

```console
$ docker pull ghost@sha256:56215ea56599da1bac73faf28a96259dc0479ae63a86ff364bbd90dcc7724e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6adac70a75f2b20757743143591caa6e38377ba58f3a19bc2720bc0c8de3073`

```dockerfile
```

-	Layers:
	-	`sha256:d1a67ed51384953de0b80812877aeafa3ab4d77d73b8d3a65a991d1c6567d6fa`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 5.6 MB (5611041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2e739425d1eef4534729048ffb99a1cfef0b1f96ea1ce2b896b9694bc38cbc5`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.5 KB (26516 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8.0` - linux; s390x

```console
$ docker pull ghost@sha256:cfd3d21d5e1501f362a50c090a0dfebfdbdbfb6a5251c68cc7866c581447b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221995814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483f844dc2b67fe79f4cc732a0b6547572e68c3e37e1660755d293490e38fa75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:33:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 03:35:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 03:35:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:35:48 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:21 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:39 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:43 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:43 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:43 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:44 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b483b0df66cd8c70ba210c61fdc3840348da24bad86177f3799a15a254e527`  
		Last Modified: Tue, 04 Nov 2025 03:34:01 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b320a6187066ba76389a7c79a1ddcb01d2b7798c2b10f4a370838218e2b7502`  
		Last Modified: Tue, 04 Nov 2025 03:36:30 GMT  
		Size: 49.7 MB (49676869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94b7e8c1441d6d3f81305d6be716fd246c56e2ffe42813414eee448bcc0db3d`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b080f614a4846400e9341eea05bfc895791733a0574b3b7a0e133f7095e26c3b`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e25b4aea4e283179ce72acb52f272e26fdc644f71a2f31d91ce19c7cb83c9a4`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 1.2 MB (1221305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b5b430011654539652162ae126fad71141236f36f4bd289668bffd636e4597`  
		Last Modified: Fri, 14 Nov 2025 17:17:56 GMT  
		Size: 11.7 MB (11676181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffba5d1b26178851461a6d7112f84646693457b752e5ee763672efed2aaa2013`  
		Last Modified: Fri, 14 Nov 2025 17:17:37 GMT  
		Size: 130.8 MB (130819971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1617d5b92e47b9096b44c75075adef4bb47445928af5b155ae01683c2375062d`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8.0` - unknown; unknown

```console
$ docker pull ghost@sha256:00547a5deba99ed2a3feaf2c865feeb31da0b741f8dad07caae3b66249f9725b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c118fdb5d65f98f9c554f78161e9cd1326cbbbbbba84d9a10d93e9a76b1a48d6`

```dockerfile
```

-	Layers:
	-	`sha256:62eab9ad244f580d8fcab14bd3eccf3e0196228bd3ccac84cf7b891b8c28b586`  
		Last Modified: Fri, 14 Nov 2025 19:45:55 GMT  
		Size: 5.6 MB (5604517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc702032869af479006fa83b52bb022c5877562d2508f26b9380b61b2e3264`  
		Last Modified: Fri, 14 Nov 2025 19:45:56 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.8.0-alpine`

```console
$ docker pull ghost@sha256:b336036a044d6e0f38427725ce777555ca05bcbefa9d51761c962edcf91242f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.8.0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:e20b75ba2535eb71b1f05f87b00d526b2832c5dca8ae9fac2b06255b8fcb0110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197462745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac976d839b348c5f7aabae4bb681c0febefa62da0eb864d526b44d77adffc28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:16:03 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:16:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:03 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:16:06 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:16:06 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:17:09 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:17:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2cca81d0de31536e59c1e347c529041866e5f6e73effbcd570f0373d4fbaf7`  
		Last Modified: Wed, 29 Oct 2025 14:16:30 GMT  
		Size: 51.6 MB (51567005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1acb8d81a6ae3f5871ce734e5b9aabd5cdb01ccb4fe07ec71c33d75bb4eb04c`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 1.3 MB (1260587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff8b913658cef54b13151d83455a1387472901b28d1f6a0adc49beb04b26ddc`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93780dcece6a389ee0fc2878ac73de722b82d44e5236349ad8019e4f57740dca`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 777.0 KB (777046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb03a2b21b7dd47b4be8e6dc3389204c91156dacd3f6a797875e0665097340`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 923.4 KB (923436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305212959a3c0bcac2d57cf3c9fa68eab4685f0849724388c08c54074e887411`  
		Last Modified: Fri, 14 Nov 2025 17:20:13 GMT  
		Size: 11.7 MB (11661070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f1d5752b1a9e4b15a37f485ed95d8e815fd7560631d635d94bc1870b8c024d`  
		Last Modified: Fri, 14 Nov 2025 17:20:23 GMT  
		Size: 127.5 MB (127470132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59a81117abbc6765eba809e22fab73ba2bf0a860700d424f912640757b34968`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c40cdcd78a9433aa57f34f01d2402e16863431b73da507d5b04b5e0e5c79a8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3423967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f452f7f944b813018ac642c5bc091e1eeddb44dec15e05ba8675b2a968355446`

```dockerfile
```

-	Layers:
	-	`sha256:50438ad815c60487c1cc97bc7ac3167a5f3d6e652cc61ee874256a215a3dcf61`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 3.4 MB (3397592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03334d8b227a09a15df71369cd9ebdb94010cad422fec9e4e8c2fc1433cab39`  
		Last Modified: Fri, 14 Nov 2025 19:45:45 GMT  
		Size: 26.4 KB (26375 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8.0-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:ff7c819bda0fb2640c79b0a3395fa6d5b67583a0838b732e0f37a1a4734dd513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208322385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494917289c9d267774521ac5599f1877801a2d35b5ae0bd97d227319b0f4495`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:59:43 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:59:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:43 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:59:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:59:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:16:37 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:16:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:16:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7f10bb4cab8241af39f5b5501c8521bff142a1639261b864dbaa26ba4f09b`  
		Last Modified: Wed, 29 Oct 2025 15:09:40 GMT  
		Size: 51.3 MB (51277073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795662ff4ed414582c3847700e3924c8c3e1f69383c1653dc45ff97289c6cdf5`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b641bc33f5a4d376a58cad5e8c1208009b85a6b638bc14778a202d5cbfbb22e0`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f73c281c8872be3944999754ac882be0234869c06ee089c16dde2b3ad94ebff`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 838.6 KB (838589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed47e17a17bcdaf0bd27a90b50ae37de58890bffad0c6502f64060b987cf750`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034be3ec0f654b3d0dbbb6aa9e92342c7cf9da326ab3f711f742e4d3dd0e336e`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 11.7 MB (11666496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975b7e8d29d8073e4f5aa72b21fd3c4ec30d6ec4ddbc09dc5f78060a11c2847`  
		Last Modified: Fri, 14 Nov 2025 19:46:24 GMT  
		Size: 138.3 MB (138264205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6207d62a7c87c88a54029cd54e92e9c31b478e57c63f35be6d1d50ed80cc91f`  
		Last Modified: Fri, 14 Nov 2025 17:20:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:6cf6f1005beec6cead8a33c5dc26ff233af69871f176b2e63bb9dd85c2a378d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141b7670455774617d465d1d7be115f9d349b19a7c95da53541bfc8b786ca1b3`

```dockerfile
```

-	Layers:
	-	`sha256:7e209584134b5a69b318a39c75a7bcb00f09b05034e0a2b51f4359118275b454`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 3.4 MB (3397748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ef1e4256639b8bcb2d7accdbc703d7fa2c0137bb4de694d06799f6135d64cf`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.6 KB (26573 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.8.0-alpine3.22`

```console
$ docker pull ghost@sha256:b336036a044d6e0f38427725ce777555ca05bcbefa9d51761c962edcf91242f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.8.0-alpine3.22` - linux; amd64

```console
$ docker pull ghost@sha256:e20b75ba2535eb71b1f05f87b00d526b2832c5dca8ae9fac2b06255b8fcb0110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197462745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac976d839b348c5f7aabae4bb681c0febefa62da0eb864d526b44d77adffc28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:16:03 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:16:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:03 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:16:06 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:16:06 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:17:09 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:17:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2cca81d0de31536e59c1e347c529041866e5f6e73effbcd570f0373d4fbaf7`  
		Last Modified: Wed, 29 Oct 2025 14:16:30 GMT  
		Size: 51.6 MB (51567005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1acb8d81a6ae3f5871ce734e5b9aabd5cdb01ccb4fe07ec71c33d75bb4eb04c`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 1.3 MB (1260587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff8b913658cef54b13151d83455a1387472901b28d1f6a0adc49beb04b26ddc`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93780dcece6a389ee0fc2878ac73de722b82d44e5236349ad8019e4f57740dca`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 777.0 KB (777046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb03a2b21b7dd47b4be8e6dc3389204c91156dacd3f6a797875e0665097340`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 923.4 KB (923436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305212959a3c0bcac2d57cf3c9fa68eab4685f0849724388c08c54074e887411`  
		Last Modified: Fri, 14 Nov 2025 17:20:13 GMT  
		Size: 11.7 MB (11661070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f1d5752b1a9e4b15a37f485ed95d8e815fd7560631d635d94bc1870b8c024d`  
		Last Modified: Fri, 14 Nov 2025 17:20:23 GMT  
		Size: 127.5 MB (127470132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59a81117abbc6765eba809e22fab73ba2bf0a860700d424f912640757b34968`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8.0-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:c40cdcd78a9433aa57f34f01d2402e16863431b73da507d5b04b5e0e5c79a8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3423967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f452f7f944b813018ac642c5bc091e1eeddb44dec15e05ba8675b2a968355446`

```dockerfile
```

-	Layers:
	-	`sha256:50438ad815c60487c1cc97bc7ac3167a5f3d6e652cc61ee874256a215a3dcf61`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 3.4 MB (3397592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03334d8b227a09a15df71369cd9ebdb94010cad422fec9e4e8c2fc1433cab39`  
		Last Modified: Fri, 14 Nov 2025 19:45:45 GMT  
		Size: 26.4 KB (26375 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8.0-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:ff7c819bda0fb2640c79b0a3395fa6d5b67583a0838b732e0f37a1a4734dd513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208322385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494917289c9d267774521ac5599f1877801a2d35b5ae0bd97d227319b0f4495`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:59:43 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:59:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:43 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:59:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:59:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:16:37 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:16:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:16:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7f10bb4cab8241af39f5b5501c8521bff142a1639261b864dbaa26ba4f09b`  
		Last Modified: Wed, 29 Oct 2025 15:09:40 GMT  
		Size: 51.3 MB (51277073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795662ff4ed414582c3847700e3924c8c3e1f69383c1653dc45ff97289c6cdf5`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b641bc33f5a4d376a58cad5e8c1208009b85a6b638bc14778a202d5cbfbb22e0`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f73c281c8872be3944999754ac882be0234869c06ee089c16dde2b3ad94ebff`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 838.6 KB (838589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed47e17a17bcdaf0bd27a90b50ae37de58890bffad0c6502f64060b987cf750`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034be3ec0f654b3d0dbbb6aa9e92342c7cf9da326ab3f711f742e4d3dd0e336e`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 11.7 MB (11666496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975b7e8d29d8073e4f5aa72b21fd3c4ec30d6ec4ddbc09dc5f78060a11c2847`  
		Last Modified: Fri, 14 Nov 2025 19:46:24 GMT  
		Size: 138.3 MB (138264205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6207d62a7c87c88a54029cd54e92e9c31b478e57c63f35be6d1d50ed80cc91f`  
		Last Modified: Fri, 14 Nov 2025 17:20:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8.0-alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:6cf6f1005beec6cead8a33c5dc26ff233af69871f176b2e63bb9dd85c2a378d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141b7670455774617d465d1d7be115f9d349b19a7c95da53541bfc8b786ca1b3`

```dockerfile
```

-	Layers:
	-	`sha256:7e209584134b5a69b318a39c75a7bcb00f09b05034e0a2b51f4359118275b454`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 3.4 MB (3397748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ef1e4256639b8bcb2d7accdbc703d7fa2c0137bb4de694d06799f6135d64cf`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.6 KB (26573 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.8.0-bookworm`

```console
$ docker pull ghost@sha256:85e15524ac7e437720fa4ac3cd4633daaae3f95786a25633415d8d4f7382b4c4
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

### `ghost:6.8.0-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:d6305ad973dec2adb1e34dc71e2306e677e9ae485826162435740e12138b353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220013893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0657b74d11a9a245eda88cdd14a1a2af921eb72358fa1f1d0e7474032933fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:34:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:34:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:37 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:15:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:15:05 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:09 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:09 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427deb858cffe936256f73e134a5baf1b4a26a93b79e03850d2243f6bc1fb302`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d65a4ff088ddf61684b1496e527c5c3accd5af20974f6dd6c3bc58a93412dc`  
		Last Modified: Tue, 04 Nov 2025 00:35:04 GMT  
		Size: 49.5 MB (49481524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6653fee0b024a9e265d5b1d360a35e40e56d7b2212c51acbf76e66c88af4e02`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 1.7 MB (1712601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b7c6f7614440681a3a5b71d3914a7eb7f5122582683ae69e336cd32f238a04`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30f248c587c9e58ca2ee47211c48b240ad9159d324a31e252758ff18b68f77`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 1.2 MB (1247558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44211e7148bae27b3894b362a850d7dd095fdafa9dbea2175f94f7a7c15ce16a`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 11.7 MB (11661069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d95e3f22588236ed74154b6d0a33a31eec2d368e9bf05f8d032fca21638741`  
		Last Modified: Fri, 14 Nov 2025 17:18:22 GMT  
		Size: 127.7 MB (127678242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77aecbe65670514cc189a958e46c069c5bfbf80f12976df53de71d4d0513f8e`  
		Last Modified: Fri, 14 Nov 2025 17:18:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:c9996812fd0e5f37e9e2b5d4bd78dec441a03998d6c7100ae32c1daea95cb9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ac2c21a42e31f5bb89ef9098d4858bf42da1e90c4699c1703c011bf04abce5`

```dockerfile
```

-	Layers:
	-	`sha256:411dbbbb7b2789695a3de35dc7167e3c3a9eaa2b74d7cb01ed3765fc5f2d0bbb`  
		Last Modified: Fri, 14 Nov 2025 19:45:37 GMT  
		Size: 5.6 MB (5610690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f4880ee6e04ecce1050ea974cb0796306623dfc25b6c84f155486f5f2aae4d`  
		Last Modified: Fri, 14 Nov 2025 19:45:38 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8.0-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:6fb588205dea09931300802a570cafedb86a09af55a54c3d750c34a2b90cede7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211470991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b993d5a857428e277dd35f395d4c38e1d228abefb335b477aa9ff18cdcd8f5a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:45:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:45:27 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:45:40 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:45:40 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:13:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:13:35 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:48 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:49 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:49 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4e79d7f6a82ac834b2b909c91adf66e2efc1389b7e127d8b803cd2a3f7c095`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce593c94118d14798314e3d79e0dfbe9a2a25e8fb36f3d425e2ac3f0aac86b80`  
		Last Modified: Tue, 04 Nov 2025 00:46:06 GMT  
		Size: 44.2 MB (44208200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6316a5dddcba87433a3ac4218d745b63913b646e0d8e387ce926ce0088397de5`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 1.7 MB (1712839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832c6ea2913823d440451db9e0d70234cfb8cd353410b97f145c0fb0a102c2d6`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9751750267a6b953a3de587887881044849607b480b85b892f2d5ab40d6181`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 1.2 MB (1214409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f797f5f0b4bb007779916de8ee6d37f7f5869bd2ace21c9e163299a6c84f4037`  
		Last Modified: Fri, 14 Nov 2025 17:17:50 GMT  
		Size: 11.7 MB (11660119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db2a424c497982a7352c6bd346313619705728b03b78e2e6363e76f063ff134`  
		Last Modified: Fri, 14 Nov 2025 20:23:39 GMT  
		Size: 128.7 MB (128736966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad36ca1c9c94347ef2e30f86a8a83344aac769110da5d73334406f3e67d3f18`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:68ae07f1cddb025b203c7329731967c2376f075be3f4506dd4c64d6882201c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd78e61405dd7e6c2f94c2cc81bec597f4756c28054a64ea6219ebfe84d1616`

```dockerfile
```

-	Layers:
	-	`sha256:37c3534eccf25aa343a7c345cd9ed2999640c0d231082055410e5e084cafd22f`  
		Last Modified: Fri, 14 Nov 2025 19:45:43 GMT  
		Size: 5.6 MB (5613489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e62a0ec9c3265208738ffd9a496a6ddd90aef3e2db9e96d344dc51c15b6e875`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 26.5 KB (26472 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:8d6f3599b40431c17606f590240838ffa35effe0109f502d2543b5c835346784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220075003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb2d4a30d3be8fb6084ffbdefd94aab83b46cf63d4ab0e0ff3e79e563436612`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:35:35 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:35:46 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:35:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:48 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:27 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce654a657d29e2be7faa623cc5a1877b6a78e8b6669ef6e9e48a54b261f2dbb1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36115b3c0ec4b3e7a273bca9f36591f9b2db12432bf4f70ad0f38fee26d12353`  
		Last Modified: Tue, 04 Nov 2025 00:36:13 GMT  
		Size: 49.6 MB (49614672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53479a8a7fd9dfad5cc88f68b7182c993f5e24b6cfc0b672e3c96b28eadc3da9`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be8e8db985232f1716a04e833933730acd9419ec49aa51c1f1aa69fe22888e1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29f9b4dcd7e856a096ca07550a76b23003c52689d12394cb194daf637fd35e8`  
		Last Modified: Fri, 14 Nov 2025 17:18:45 GMT  
		Size: 1.2 MB (1201445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e917f52639864038fbd445a1047ab571f36715192e655b1d5e33925a16354f`  
		Last Modified: Fri, 14 Nov 2025 17:18:46 GMT  
		Size: 11.7 MB (11666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567d8828b01841392dcf0dec341fe287fbf97ce1e1929e6e32dd8695d51b257d`  
		Last Modified: Fri, 14 Nov 2025 17:19:04 GMT  
		Size: 127.8 MB (127772964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3222ac9c7fc4d2dd2ab35916c7a28642609a55b223c5157379fb85bc15a2cebd`  
		Last Modified: Fri, 14 Nov 2025 17:18:44 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:56215ea56599da1bac73faf28a96259dc0479ae63a86ff364bbd90dcc7724e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6adac70a75f2b20757743143591caa6e38377ba58f3a19bc2720bc0c8de3073`

```dockerfile
```

-	Layers:
	-	`sha256:d1a67ed51384953de0b80812877aeafa3ab4d77d73b8d3a65a991d1c6567d6fa`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 5.6 MB (5611041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2e739425d1eef4534729048ffb99a1cfef0b1f96ea1ce2b896b9694bc38cbc5`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.5 KB (26516 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.8.0-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:cfd3d21d5e1501f362a50c090a0dfebfdbdbfb6a5251c68cc7866c581447b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221995814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483f844dc2b67fe79f4cc732a0b6547572e68c3e37e1660755d293490e38fa75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:33:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 03:35:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 03:35:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:35:48 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:21 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:39 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:43 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:43 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:43 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:44 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b483b0df66cd8c70ba210c61fdc3840348da24bad86177f3799a15a254e527`  
		Last Modified: Tue, 04 Nov 2025 03:34:01 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b320a6187066ba76389a7c79a1ddcb01d2b7798c2b10f4a370838218e2b7502`  
		Last Modified: Tue, 04 Nov 2025 03:36:30 GMT  
		Size: 49.7 MB (49676869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94b7e8c1441d6d3f81305d6be716fd246c56e2ffe42813414eee448bcc0db3d`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b080f614a4846400e9341eea05bfc895791733a0574b3b7a0e133f7095e26c3b`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e25b4aea4e283179ce72acb52f272e26fdc644f71a2f31d91ce19c7cb83c9a4`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 1.2 MB (1221305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b5b430011654539652162ae126fad71141236f36f4bd289668bffd636e4597`  
		Last Modified: Fri, 14 Nov 2025 17:17:56 GMT  
		Size: 11.7 MB (11676181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffba5d1b26178851461a6d7112f84646693457b752e5ee763672efed2aaa2013`  
		Last Modified: Fri, 14 Nov 2025 17:17:37 GMT  
		Size: 130.8 MB (130819971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1617d5b92e47b9096b44c75075adef4bb47445928af5b155ae01683c2375062d`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.8.0-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:00547a5deba99ed2a3feaf2c865feeb31da0b741f8dad07caae3b66249f9725b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c118fdb5d65f98f9c554f78161e9cd1326cbbbbbba84d9a10d93e9a76b1a48d6`

```dockerfile
```

-	Layers:
	-	`sha256:62eab9ad244f580d8fcab14bd3eccf3e0196228bd3ccac84cf7b891b8c28b586`  
		Last Modified: Fri, 14 Nov 2025 19:45:55 GMT  
		Size: 5.6 MB (5604517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc702032869af479006fa83b52bb022c5877562d2508f26b9380b61b2e3264`  
		Last Modified: Fri, 14 Nov 2025 19:45:56 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine`

```console
$ docker pull ghost@sha256:b336036a044d6e0f38427725ce777555ca05bcbefa9d51761c962edcf91242f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:e20b75ba2535eb71b1f05f87b00d526b2832c5dca8ae9fac2b06255b8fcb0110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197462745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac976d839b348c5f7aabae4bb681c0febefa62da0eb864d526b44d77adffc28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:16:03 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:16:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:03 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:16:06 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:16:06 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:17:09 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:17:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2cca81d0de31536e59c1e347c529041866e5f6e73effbcd570f0373d4fbaf7`  
		Last Modified: Wed, 29 Oct 2025 14:16:30 GMT  
		Size: 51.6 MB (51567005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1acb8d81a6ae3f5871ce734e5b9aabd5cdb01ccb4fe07ec71c33d75bb4eb04c`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 1.3 MB (1260587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff8b913658cef54b13151d83455a1387472901b28d1f6a0adc49beb04b26ddc`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93780dcece6a389ee0fc2878ac73de722b82d44e5236349ad8019e4f57740dca`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 777.0 KB (777046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb03a2b21b7dd47b4be8e6dc3389204c91156dacd3f6a797875e0665097340`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 923.4 KB (923436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305212959a3c0bcac2d57cf3c9fa68eab4685f0849724388c08c54074e887411`  
		Last Modified: Fri, 14 Nov 2025 17:20:13 GMT  
		Size: 11.7 MB (11661070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f1d5752b1a9e4b15a37f485ed95d8e815fd7560631d635d94bc1870b8c024d`  
		Last Modified: Fri, 14 Nov 2025 17:20:23 GMT  
		Size: 127.5 MB (127470132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59a81117abbc6765eba809e22fab73ba2bf0a860700d424f912640757b34968`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c40cdcd78a9433aa57f34f01d2402e16863431b73da507d5b04b5e0e5c79a8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3423967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f452f7f944b813018ac642c5bc091e1eeddb44dec15e05ba8675b2a968355446`

```dockerfile
```

-	Layers:
	-	`sha256:50438ad815c60487c1cc97bc7ac3167a5f3d6e652cc61ee874256a215a3dcf61`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 3.4 MB (3397592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03334d8b227a09a15df71369cd9ebdb94010cad422fec9e4e8c2fc1433cab39`  
		Last Modified: Fri, 14 Nov 2025 19:45:45 GMT  
		Size: 26.4 KB (26375 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:ff7c819bda0fb2640c79b0a3395fa6d5b67583a0838b732e0f37a1a4734dd513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208322385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494917289c9d267774521ac5599f1877801a2d35b5ae0bd97d227319b0f4495`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:59:43 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:59:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:43 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:59:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:59:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:16:37 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:16:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:16:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7f10bb4cab8241af39f5b5501c8521bff142a1639261b864dbaa26ba4f09b`  
		Last Modified: Wed, 29 Oct 2025 15:09:40 GMT  
		Size: 51.3 MB (51277073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795662ff4ed414582c3847700e3924c8c3e1f69383c1653dc45ff97289c6cdf5`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b641bc33f5a4d376a58cad5e8c1208009b85a6b638bc14778a202d5cbfbb22e0`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f73c281c8872be3944999754ac882be0234869c06ee089c16dde2b3ad94ebff`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 838.6 KB (838589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed47e17a17bcdaf0bd27a90b50ae37de58890bffad0c6502f64060b987cf750`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034be3ec0f654b3d0dbbb6aa9e92342c7cf9da326ab3f711f742e4d3dd0e336e`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 11.7 MB (11666496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975b7e8d29d8073e4f5aa72b21fd3c4ec30d6ec4ddbc09dc5f78060a11c2847`  
		Last Modified: Fri, 14 Nov 2025 19:46:24 GMT  
		Size: 138.3 MB (138264205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6207d62a7c87c88a54029cd54e92e9c31b478e57c63f35be6d1d50ed80cc91f`  
		Last Modified: Fri, 14 Nov 2025 17:20:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:6cf6f1005beec6cead8a33c5dc26ff233af69871f176b2e63bb9dd85c2a378d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141b7670455774617d465d1d7be115f9d349b19a7c95da53541bfc8b786ca1b3`

```dockerfile
```

-	Layers:
	-	`sha256:7e209584134b5a69b318a39c75a7bcb00f09b05034e0a2b51f4359118275b454`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 3.4 MB (3397748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ef1e4256639b8bcb2d7accdbc703d7fa2c0137bb4de694d06799f6135d64cf`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.6 KB (26573 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine3.22`

```console
$ docker pull ghost@sha256:b336036a044d6e0f38427725ce777555ca05bcbefa9d51761c962edcf91242f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine3.22` - linux; amd64

```console
$ docker pull ghost@sha256:e20b75ba2535eb71b1f05f87b00d526b2832c5dca8ae9fac2b06255b8fcb0110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197462745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac976d839b348c5f7aabae4bb681c0febefa62da0eb864d526b44d77adffc28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:16:03 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:16:03 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:03 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:16:06 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:16:06 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:17:09 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:17:12 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:17:12 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:17:21 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:17:21 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:26 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2cca81d0de31536e59c1e347c529041866e5f6e73effbcd570f0373d4fbaf7`  
		Last Modified: Wed, 29 Oct 2025 14:16:30 GMT  
		Size: 51.6 MB (51567005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1acb8d81a6ae3f5871ce734e5b9aabd5cdb01ccb4fe07ec71c33d75bb4eb04c`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 1.3 MB (1260587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff8b913658cef54b13151d83455a1387472901b28d1f6a0adc49beb04b26ddc`  
		Last Modified: Wed, 29 Oct 2025 14:16:25 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93780dcece6a389ee0fc2878ac73de722b82d44e5236349ad8019e4f57740dca`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 777.0 KB (777046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb03a2b21b7dd47b4be8e6dc3389204c91156dacd3f6a797875e0665097340`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 923.4 KB (923436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305212959a3c0bcac2d57cf3c9fa68eab4685f0849724388c08c54074e887411`  
		Last Modified: Fri, 14 Nov 2025 17:20:13 GMT  
		Size: 11.7 MB (11661070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f1d5752b1a9e4b15a37f485ed95d8e815fd7560631d635d94bc1870b8c024d`  
		Last Modified: Fri, 14 Nov 2025 17:20:23 GMT  
		Size: 127.5 MB (127470132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59a81117abbc6765eba809e22fab73ba2bf0a860700d424f912640757b34968`  
		Last Modified: Fri, 14 Nov 2025 17:20:12 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:c40cdcd78a9433aa57f34f01d2402e16863431b73da507d5b04b5e0e5c79a8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3423967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f452f7f944b813018ac642c5bc091e1eeddb44dec15e05ba8675b2a968355446`

```dockerfile
```

-	Layers:
	-	`sha256:50438ad815c60487c1cc97bc7ac3167a5f3d6e652cc61ee874256a215a3dcf61`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 3.4 MB (3397592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03334d8b227a09a15df71369cd9ebdb94010cad422fec9e4e8c2fc1433cab39`  
		Last Modified: Fri, 14 Nov 2025 19:45:45 GMT  
		Size: 26.4 KB (26375 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:ff7c819bda0fb2640c79b0a3395fa6d5b67583a0838b732e0f37a1a4734dd513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208322385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8494917289c9d267774521ac5599f1877801a2d35b5ae0bd97d227319b0f4495`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 14:59:43 GMT
ENV NODE_VERSION=22.21.1
# Wed, 29 Oct 2025 14:59:43 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="8c684c3a58f4bb0f1513dd288608e47e16349999f6525843d9ef72d67410b15d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:43 GMT
ENV YARN_VERSION=1.22.22
# Wed, 29 Oct 2025 14:59:46 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Oct 2025 14:59:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Oct 2025 14:59:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:16:37 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:16:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:16:40 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:16:40 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:16:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:16:54 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:19:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:19:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:19:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:19:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:19:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:19:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7f10bb4cab8241af39f5b5501c8521bff142a1639261b864dbaa26ba4f09b`  
		Last Modified: Wed, 29 Oct 2025 15:09:40 GMT  
		Size: 51.3 MB (51277073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795662ff4ed414582c3847700e3924c8c3e1f69383c1653dc45ff97289c6cdf5`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b641bc33f5a4d376a58cad5e8c1208009b85a6b638bc14778a202d5cbfbb22e0`  
		Last Modified: Wed, 29 Oct 2025 15:09:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f73c281c8872be3944999754ac882be0234869c06ee089c16dde2b3ad94ebff`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 838.6 KB (838589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed47e17a17bcdaf0bd27a90b50ae37de58890bffad0c6502f64060b987cf750`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 876.4 KB (876371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034be3ec0f654b3d0dbbb6aa9e92342c7cf9da326ab3f711f742e4d3dd0e336e`  
		Last Modified: Fri, 14 Nov 2025 17:20:43 GMT  
		Size: 11.7 MB (11666496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975b7e8d29d8073e4f5aa72b21fd3c4ec30d6ec4ddbc09dc5f78060a11c2847`  
		Last Modified: Fri, 14 Nov 2025 19:46:24 GMT  
		Size: 138.3 MB (138264205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6207d62a7c87c88a54029cd54e92e9c31b478e57c63f35be6d1d50ed80cc91f`  
		Last Modified: Fri, 14 Nov 2025 17:20:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.22` - unknown; unknown

```console
$ docker pull ghost@sha256:6cf6f1005beec6cead8a33c5dc26ff233af69871f176b2e63bb9dd85c2a378d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3424321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141b7670455774617d465d1d7be115f9d349b19a7c95da53541bfc8b786ca1b3`

```dockerfile
```

-	Layers:
	-	`sha256:7e209584134b5a69b318a39c75a7bcb00f09b05034e0a2b51f4359118275b454`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 3.4 MB (3397748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ef1e4256639b8bcb2d7accdbc703d7fa2c0137bb4de694d06799f6135d64cf`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.6 KB (26573 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:bookworm`

```console
$ docker pull ghost@sha256:85e15524ac7e437720fa4ac3cd4633daaae3f95786a25633415d8d4f7382b4c4
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
$ docker pull ghost@sha256:d6305ad973dec2adb1e34dc71e2306e677e9ae485826162435740e12138b353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220013893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0657b74d11a9a245eda88cdd14a1a2af921eb72358fa1f1d0e7474032933fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:34:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:34:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:37 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:15:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:15:05 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:09 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:09 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427deb858cffe936256f73e134a5baf1b4a26a93b79e03850d2243f6bc1fb302`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d65a4ff088ddf61684b1496e527c5c3accd5af20974f6dd6c3bc58a93412dc`  
		Last Modified: Tue, 04 Nov 2025 00:35:04 GMT  
		Size: 49.5 MB (49481524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6653fee0b024a9e265d5b1d360a35e40e56d7b2212c51acbf76e66c88af4e02`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 1.7 MB (1712601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b7c6f7614440681a3a5b71d3914a7eb7f5122582683ae69e336cd32f238a04`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30f248c587c9e58ca2ee47211c48b240ad9159d324a31e252758ff18b68f77`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 1.2 MB (1247558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44211e7148bae27b3894b362a850d7dd095fdafa9dbea2175f94f7a7c15ce16a`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 11.7 MB (11661069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d95e3f22588236ed74154b6d0a33a31eec2d368e9bf05f8d032fca21638741`  
		Last Modified: Fri, 14 Nov 2025 17:18:22 GMT  
		Size: 127.7 MB (127678242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77aecbe65670514cc189a958e46c069c5bfbf80f12976df53de71d4d0513f8e`  
		Last Modified: Fri, 14 Nov 2025 17:18:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:c9996812fd0e5f37e9e2b5d4bd78dec441a03998d6c7100ae32c1daea95cb9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ac2c21a42e31f5bb89ef9098d4858bf42da1e90c4699c1703c011bf04abce5`

```dockerfile
```

-	Layers:
	-	`sha256:411dbbbb7b2789695a3de35dc7167e3c3a9eaa2b74d7cb01ed3765fc5f2d0bbb`  
		Last Modified: Fri, 14 Nov 2025 19:45:37 GMT  
		Size: 5.6 MB (5610690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f4880ee6e04ecce1050ea974cb0796306623dfc25b6c84f155486f5f2aae4d`  
		Last Modified: Fri, 14 Nov 2025 19:45:38 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:6fb588205dea09931300802a570cafedb86a09af55a54c3d750c34a2b90cede7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211470991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b993d5a857428e277dd35f395d4c38e1d228abefb335b477aa9ff18cdcd8f5a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:45:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:45:27 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:45:40 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:45:40 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:13:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:13:35 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:48 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:49 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:49 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4e79d7f6a82ac834b2b909c91adf66e2efc1389b7e127d8b803cd2a3f7c095`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce593c94118d14798314e3d79e0dfbe9a2a25e8fb36f3d425e2ac3f0aac86b80`  
		Last Modified: Tue, 04 Nov 2025 00:46:06 GMT  
		Size: 44.2 MB (44208200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6316a5dddcba87433a3ac4218d745b63913b646e0d8e387ce926ce0088397de5`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 1.7 MB (1712839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832c6ea2913823d440451db9e0d70234cfb8cd353410b97f145c0fb0a102c2d6`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9751750267a6b953a3de587887881044849607b480b85b892f2d5ab40d6181`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 1.2 MB (1214409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f797f5f0b4bb007779916de8ee6d37f7f5869bd2ace21c9e163299a6c84f4037`  
		Last Modified: Fri, 14 Nov 2025 17:17:50 GMT  
		Size: 11.7 MB (11660119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db2a424c497982a7352c6bd346313619705728b03b78e2e6363e76f063ff134`  
		Last Modified: Fri, 14 Nov 2025 20:23:39 GMT  
		Size: 128.7 MB (128736966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad36ca1c9c94347ef2e30f86a8a83344aac769110da5d73334406f3e67d3f18`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:68ae07f1cddb025b203c7329731967c2376f075be3f4506dd4c64d6882201c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd78e61405dd7e6c2f94c2cc81bec597f4756c28054a64ea6219ebfe84d1616`

```dockerfile
```

-	Layers:
	-	`sha256:37c3534eccf25aa343a7c345cd9ed2999640c0d231082055410e5e084cafd22f`  
		Last Modified: Fri, 14 Nov 2025 19:45:43 GMT  
		Size: 5.6 MB (5613489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e62a0ec9c3265208738ffd9a496a6ddd90aef3e2db9e96d344dc51c15b6e875`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 26.5 KB (26472 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:8d6f3599b40431c17606f590240838ffa35effe0109f502d2543b5c835346784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220075003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb2d4a30d3be8fb6084ffbdefd94aab83b46cf63d4ab0e0ff3e79e563436612`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:35:35 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:35:46 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:35:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:48 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:27 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce654a657d29e2be7faa623cc5a1877b6a78e8b6669ef6e9e48a54b261f2dbb1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36115b3c0ec4b3e7a273bca9f36591f9b2db12432bf4f70ad0f38fee26d12353`  
		Last Modified: Tue, 04 Nov 2025 00:36:13 GMT  
		Size: 49.6 MB (49614672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53479a8a7fd9dfad5cc88f68b7182c993f5e24b6cfc0b672e3c96b28eadc3da9`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be8e8db985232f1716a04e833933730acd9419ec49aa51c1f1aa69fe22888e1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29f9b4dcd7e856a096ca07550a76b23003c52689d12394cb194daf637fd35e8`  
		Last Modified: Fri, 14 Nov 2025 17:18:45 GMT  
		Size: 1.2 MB (1201445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e917f52639864038fbd445a1047ab571f36715192e655b1d5e33925a16354f`  
		Last Modified: Fri, 14 Nov 2025 17:18:46 GMT  
		Size: 11.7 MB (11666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567d8828b01841392dcf0dec341fe287fbf97ce1e1929e6e32dd8695d51b257d`  
		Last Modified: Fri, 14 Nov 2025 17:19:04 GMT  
		Size: 127.8 MB (127772964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3222ac9c7fc4d2dd2ab35916c7a28642609a55b223c5157379fb85bc15a2cebd`  
		Last Modified: Fri, 14 Nov 2025 17:18:44 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:56215ea56599da1bac73faf28a96259dc0479ae63a86ff364bbd90dcc7724e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6adac70a75f2b20757743143591caa6e38377ba58f3a19bc2720bc0c8de3073`

```dockerfile
```

-	Layers:
	-	`sha256:d1a67ed51384953de0b80812877aeafa3ab4d77d73b8d3a65a991d1c6567d6fa`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 5.6 MB (5611041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2e739425d1eef4534729048ffb99a1cfef0b1f96ea1ce2b896b9694bc38cbc5`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.5 KB (26516 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:cfd3d21d5e1501f362a50c090a0dfebfdbdbfb6a5251c68cc7866c581447b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221995814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483f844dc2b67fe79f4cc732a0b6547572e68c3e37e1660755d293490e38fa75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:33:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 03:35:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 03:35:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:35:48 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:21 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:39 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:43 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:43 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:43 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:44 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b483b0df66cd8c70ba210c61fdc3840348da24bad86177f3799a15a254e527`  
		Last Modified: Tue, 04 Nov 2025 03:34:01 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b320a6187066ba76389a7c79a1ddcb01d2b7798c2b10f4a370838218e2b7502`  
		Last Modified: Tue, 04 Nov 2025 03:36:30 GMT  
		Size: 49.7 MB (49676869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94b7e8c1441d6d3f81305d6be716fd246c56e2ffe42813414eee448bcc0db3d`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b080f614a4846400e9341eea05bfc895791733a0574b3b7a0e133f7095e26c3b`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e25b4aea4e283179ce72acb52f272e26fdc644f71a2f31d91ce19c7cb83c9a4`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 1.2 MB (1221305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b5b430011654539652162ae126fad71141236f36f4bd289668bffd636e4597`  
		Last Modified: Fri, 14 Nov 2025 17:17:56 GMT  
		Size: 11.7 MB (11676181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffba5d1b26178851461a6d7112f84646693457b752e5ee763672efed2aaa2013`  
		Last Modified: Fri, 14 Nov 2025 17:17:37 GMT  
		Size: 130.8 MB (130819971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1617d5b92e47b9096b44c75075adef4bb47445928af5b155ae01683c2375062d`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:00547a5deba99ed2a3feaf2c865feeb31da0b741f8dad07caae3b66249f9725b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c118fdb5d65f98f9c554f78161e9cd1326cbbbbbba84d9a10d93e9a76b1a48d6`

```dockerfile
```

-	Layers:
	-	`sha256:62eab9ad244f580d8fcab14bd3eccf3e0196228bd3ccac84cf7b891b8c28b586`  
		Last Modified: Fri, 14 Nov 2025 19:45:55 GMT  
		Size: 5.6 MB (5604517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc702032869af479006fa83b52bb022c5877562d2508f26b9380b61b2e3264`  
		Last Modified: Fri, 14 Nov 2025 19:45:56 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:latest`

```console
$ docker pull ghost@sha256:85e15524ac7e437720fa4ac3cd4633daaae3f95786a25633415d8d4f7382b4c4
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
$ docker pull ghost@sha256:d6305ad973dec2adb1e34dc71e2306e677e9ae485826162435740e12138b353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220013893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0657b74d11a9a245eda88cdd14a1a2af921eb72358fa1f1d0e7474032933fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:34:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:26 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:34:37 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:37 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:15:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:15:05 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:15:05 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:15 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:15 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:09 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:09 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:09 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:09 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427deb858cffe936256f73e134a5baf1b4a26a93b79e03850d2243f6bc1fb302`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d65a4ff088ddf61684b1496e527c5c3accd5af20974f6dd6c3bc58a93412dc`  
		Last Modified: Tue, 04 Nov 2025 00:35:04 GMT  
		Size: 49.5 MB (49481524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6653fee0b024a9e265d5b1d360a35e40e56d7b2212c51acbf76e66c88af4e02`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 1.7 MB (1712601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b7c6f7614440681a3a5b71d3914a7eb7f5122582683ae69e336cd32f238a04`  
		Last Modified: Tue, 04 Nov 2025 00:34:55 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30f248c587c9e58ca2ee47211c48b240ad9159d324a31e252758ff18b68f77`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 1.2 MB (1247558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44211e7148bae27b3894b362a850d7dd095fdafa9dbea2175f94f7a7c15ce16a`  
		Last Modified: Fri, 14 Nov 2025 17:18:12 GMT  
		Size: 11.7 MB (11661069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d95e3f22588236ed74154b6d0a33a31eec2d368e9bf05f8d032fca21638741`  
		Last Modified: Fri, 14 Nov 2025 17:18:22 GMT  
		Size: 127.7 MB (127678242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77aecbe65670514cc189a958e46c069c5bfbf80f12976df53de71d4d0513f8e`  
		Last Modified: Fri, 14 Nov 2025 17:18:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:c9996812fd0e5f37e9e2b5d4bd78dec441a03998d6c7100ae32c1daea95cb9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ac2c21a42e31f5bb89ef9098d4858bf42da1e90c4699c1703c011bf04abce5`

```dockerfile
```

-	Layers:
	-	`sha256:411dbbbb7b2789695a3de35dc7167e3c3a9eaa2b74d7cb01ed3765fc5f2d0bbb`  
		Last Modified: Fri, 14 Nov 2025 19:45:37 GMT  
		Size: 5.6 MB (5610690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f4880ee6e04ecce1050ea974cb0796306623dfc25b6c84f155486f5f2aae4d`  
		Last Modified: Fri, 14 Nov 2025 19:45:38 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:6fb588205dea09931300802a570cafedb86a09af55a54c3d750c34a2b90cede7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211470991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b993d5a857428e277dd35f395d4c38e1d228abefb335b477aa9ff18cdcd8f5a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:45:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:45:27 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:27 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:45:40 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:45:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:45:40 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:13:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:13:35 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:13:35 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:00 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:00 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:48 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:49 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:49 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:49 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4e79d7f6a82ac834b2b909c91adf66e2efc1389b7e127d8b803cd2a3f7c095`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce593c94118d14798314e3d79e0dfbe9a2a25e8fb36f3d425e2ac3f0aac86b80`  
		Last Modified: Tue, 04 Nov 2025 00:46:06 GMT  
		Size: 44.2 MB (44208200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6316a5dddcba87433a3ac4218d745b63913b646e0d8e387ce926ce0088397de5`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 1.7 MB (1712839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832c6ea2913823d440451db9e0d70234cfb8cd353410b97f145c0fb0a102c2d6`  
		Last Modified: Tue, 04 Nov 2025 00:46:01 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9751750267a6b953a3de587887881044849607b480b85b892f2d5ab40d6181`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 1.2 MB (1214409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f797f5f0b4bb007779916de8ee6d37f7f5869bd2ace21c9e163299a6c84f4037`  
		Last Modified: Fri, 14 Nov 2025 17:17:50 GMT  
		Size: 11.7 MB (11660119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db2a424c497982a7352c6bd346313619705728b03b78e2e6363e76f063ff134`  
		Last Modified: Fri, 14 Nov 2025 20:23:39 GMT  
		Size: 128.7 MB (128736966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad36ca1c9c94347ef2e30f86a8a83344aac769110da5d73334406f3e67d3f18`  
		Last Modified: Fri, 14 Nov 2025 17:17:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:68ae07f1cddb025b203c7329731967c2376f075be3f4506dd4c64d6882201c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd78e61405dd7e6c2f94c2cc81bec597f4756c28054a64ea6219ebfe84d1616`

```dockerfile
```

-	Layers:
	-	`sha256:37c3534eccf25aa343a7c345cd9ed2999640c0d231082055410e5e084cafd22f`  
		Last Modified: Fri, 14 Nov 2025 19:45:43 GMT  
		Size: 5.6 MB (5613489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e62a0ec9c3265208738ffd9a496a6ddd90aef3e2db9e96d344dc51c15b6e875`  
		Last Modified: Fri, 14 Nov 2025 19:45:44 GMT  
		Size: 26.5 KB (26472 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:8d6f3599b40431c17606f590240838ffa35effe0109f502d2543b5c835346784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220075003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb2d4a30d3be8fb6084ffbdefd94aab83b46cf63d4ab0e0ff3e79e563436612`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 00:35:35 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:35 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 00:35:46 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:35:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:35:46 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:48 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:48 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:15:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:15:01 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:17:27 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:17:27 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:17:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:17:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:17:27 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:17:27 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce654a657d29e2be7faa623cc5a1877b6a78e8b6669ef6e9e48a54b261f2dbb1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36115b3c0ec4b3e7a273bca9f36591f9b2db12432bf4f70ad0f38fee26d12353`  
		Last Modified: Tue, 04 Nov 2025 00:36:13 GMT  
		Size: 49.6 MB (49614672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53479a8a7fd9dfad5cc88f68b7182c993f5e24b6cfc0b672e3c96b28eadc3da9`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be8e8db985232f1716a04e833933730acd9419ec49aa51c1f1aa69fe22888e1`  
		Last Modified: Tue, 04 Nov 2025 00:36:09 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29f9b4dcd7e856a096ca07550a76b23003c52689d12394cb194daf637fd35e8`  
		Last Modified: Fri, 14 Nov 2025 17:18:45 GMT  
		Size: 1.2 MB (1201445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e917f52639864038fbd445a1047ab571f36715192e655b1d5e33925a16354f`  
		Last Modified: Fri, 14 Nov 2025 17:18:46 GMT  
		Size: 11.7 MB (11666606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567d8828b01841392dcf0dec341fe287fbf97ce1e1929e6e32dd8695d51b257d`  
		Last Modified: Fri, 14 Nov 2025 17:19:04 GMT  
		Size: 127.8 MB (127772964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3222ac9c7fc4d2dd2ab35916c7a28642609a55b223c5157379fb85bc15a2cebd`  
		Last Modified: Fri, 14 Nov 2025 17:18:44 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:56215ea56599da1bac73faf28a96259dc0479ae63a86ff364bbd90dcc7724e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6adac70a75f2b20757743143591caa6e38377ba58f3a19bc2720bc0c8de3073`

```dockerfile
```

-	Layers:
	-	`sha256:d1a67ed51384953de0b80812877aeafa3ab4d77d73b8d3a65a991d1c6567d6fa`  
		Last Modified: Fri, 14 Nov 2025 19:45:49 GMT  
		Size: 5.6 MB (5611041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2e739425d1eef4534729048ffb99a1cfef0b1f96ea1ce2b896b9694bc38cbc5`  
		Last Modified: Fri, 14 Nov 2025 19:45:50 GMT  
		Size: 26.5 KB (26516 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:cfd3d21d5e1501f362a50c090a0dfebfdbdbfb6a5251c68cc7866c581447b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221995814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483f844dc2b67fe79f4cc732a0b6547572e68c3e37e1660755d293490e38fa75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:33:01 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV NODE_VERSION=22.21.1
# Tue, 04 Nov 2025 03:35:39 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:39 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 03:35:47 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:35:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:35:48 GMT
CMD ["node"]
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 17:14:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 17:14:21 GMT
ENV NODE_ENV=production
# Fri, 14 Nov 2025 17:14:21 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 14 Nov 2025 17:14:39 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 14 Nov 2025 17:14:39 GMT
ENV GHOST_VERSION=6.8.0
# Fri, 14 Nov 2025 17:16:43 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 14 Nov 2025 17:16:43 GMT
WORKDIR /var/lib/ghost
# Fri, 14 Nov 2025 17:16:43 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 14 Nov 2025 17:16:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:16:44 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 14 Nov 2025 17:16:44 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b483b0df66cd8c70ba210c61fdc3840348da24bad86177f3799a15a254e527`  
		Last Modified: Tue, 04 Nov 2025 03:34:01 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b320a6187066ba76389a7c79a1ddcb01d2b7798c2b10f4a370838218e2b7502`  
		Last Modified: Tue, 04 Nov 2025 03:36:30 GMT  
		Size: 49.7 MB (49676869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94b7e8c1441d6d3f81305d6be716fd246c56e2ffe42813414eee448bcc0db3d`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 1.7 MB (1712610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b080f614a4846400e9341eea05bfc895791733a0574b3b7a0e133f7095e26c3b`  
		Last Modified: Tue, 04 Nov 2025 03:36:26 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e25b4aea4e283179ce72acb52f272e26fdc644f71a2f31d91ce19c7cb83c9a4`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 1.2 MB (1221305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b5b430011654539652162ae126fad71141236f36f4bd289668bffd636e4597`  
		Last Modified: Fri, 14 Nov 2025 17:17:56 GMT  
		Size: 11.7 MB (11676181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffba5d1b26178851461a6d7112f84646693457b752e5ee763672efed2aaa2013`  
		Last Modified: Fri, 14 Nov 2025 17:17:37 GMT  
		Size: 130.8 MB (130819971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1617d5b92e47b9096b44c75075adef4bb47445928af5b155ae01683c2375062d`  
		Last Modified: Fri, 14 Nov 2025 17:17:55 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:00547a5deba99ed2a3feaf2c865feeb31da0b741f8dad07caae3b66249f9725b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c118fdb5d65f98f9c554f78161e9cd1326cbbbbbba84d9a10d93e9a76b1a48d6`

```dockerfile
```

-	Layers:
	-	`sha256:62eab9ad244f580d8fcab14bd3eccf3e0196228bd3ccac84cf7b891b8c28b586`  
		Last Modified: Fri, 14 Nov 2025 19:45:55 GMT  
		Size: 5.6 MB (5604517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc702032869af479006fa83b52bb022c5877562d2508f26b9380b61b2e3264`  
		Last Modified: Fri, 14 Nov 2025 19:45:56 GMT  
		Size: 26.3 KB (26334 bytes)  
		MIME: application/vnd.in-toto+json

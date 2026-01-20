<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:5`](#ghost5)
-	[`ghost:5-alpine`](#ghost5-alpine)
-	[`ghost:5-alpine3.23`](#ghost5-alpine323)
-	[`ghost:5-bookworm`](#ghost5-bookworm)
-	[`ghost:5.130`](#ghost5130)
-	[`ghost:5.130-alpine`](#ghost5130-alpine)
-	[`ghost:5.130-alpine3.23`](#ghost5130-alpine323)
-	[`ghost:5.130-bookworm`](#ghost5130-bookworm)
-	[`ghost:5.130.6`](#ghost51306)
-	[`ghost:5.130.6-alpine`](#ghost51306-alpine)
-	[`ghost:5.130.6-alpine3.23`](#ghost51306-alpine323)
-	[`ghost:5.130.6-bookworm`](#ghost51306-bookworm)
-	[`ghost:6`](#ghost6)
-	[`ghost:6-alpine`](#ghost6-alpine)
-	[`ghost:6-alpine3.23`](#ghost6-alpine323)
-	[`ghost:6-bookworm`](#ghost6-bookworm)
-	[`ghost:6.13`](#ghost613)
-	[`ghost:6.13-alpine`](#ghost613-alpine)
-	[`ghost:6.13-alpine3.23`](#ghost613-alpine323)
-	[`ghost:6.13-bookworm`](#ghost613-bookworm)
-	[`ghost:6.13.2`](#ghost6132)
-	[`ghost:6.13.2-alpine`](#ghost6132-alpine)
-	[`ghost:6.13.2-alpine3.23`](#ghost6132-alpine323)
-	[`ghost:6.13.2-bookworm`](#ghost6132-bookworm)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:alpine3.23`](#ghostalpine323)
-	[`ghost:bookworm`](#ghostbookworm)
-	[`ghost:latest`](#ghostlatest)

## `ghost:5`

```console
$ docker pull ghost@sha256:febc30a0a2dd702d9c625c76ce06c623e863ddf4adc225207a9f6a7983af2f1f
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
$ docker pull ghost@sha256:cd75c4c53872d65e5ad4aa0192ff7e06ffb838d6e9c3da32c377d67c9638c2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201329353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a261a521c9c9852b5853931a719ef8fee44d5eae6cd9443756a46de2e0d6b4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:59:41 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 18:00:00 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:00:00 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:00:00 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:00:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:00:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:00:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:00:12 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:18:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:18:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:18:03 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:18:03 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:18:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:19:21 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:19:22 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:19:22 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:19:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:19:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:19:22 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:19:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b9523dc7f8055cf2750f04c65434cae8f1b05241e73a5f0878d117366ad8a`  
		Last Modified: Wed, 14 Jan 2026 18:00:26 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe53019ce11f9bf83b30d24ab04d6dc4aa05dedf8c520e04da0559608edeade`  
		Last Modified: Wed, 14 Jan 2026 18:00:41 GMT  
		Size: 41.0 MB (40982889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98168ca575a7f9a177a9348c0ff4ed8e5c9ca39eb648a0654dd3c29928412cf`  
		Last Modified: Wed, 14 Jan 2026 18:00:36 GMT  
		Size: 1.7 MB (1712658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d393bf487b04ce90e509f8c13715578b3c9785f7aa2ba9bcd797b5a50c0e731`  
		Last Modified: Wed, 14 Jan 2026 18:00:36 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702e15ae043f817422edb4562290d19f8e3c32af780cb10a7b282c3fbfd33229`  
		Last Modified: Wed, 14 Jan 2026 18:19:54 GMT  
		Size: 1.2 MB (1247526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc785f759f72294cb94bba72eb544eae8fa9089e1b63e84617c4734a350ae3fc`  
		Last Modified: Wed, 14 Jan 2026 18:20:07 GMT  
		Size: 11.1 MB (11130104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a230df14864bc5e101a75973ad2d959247bef61a75d16c7dbe67434e4e797827`  
		Last Modified: Wed, 14 Jan 2026 18:20:21 GMT  
		Size: 118.0 MB (118023275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9727a9a33d14a10eaaa91e3ef41ef973e897614d2baf36d19cd5e6c52ec75`  
		Last Modified: Wed, 14 Jan 2026 18:20:05 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:fefa43decb4bf4f70e892fdb14ec6e62534005addeec7d877b8e1861ffc0afa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c342ab01f17491e38b2185ce253fe064b56729fe4445f5d94e627c3203d85e1d`

```dockerfile
```

-	Layers:
	-	`sha256:c6da51f12795fa5fa6b7125e01ed6e0814c53906dd20709c03421507b5c72c13`  
		Last Modified: Wed, 14 Jan 2026 22:45:31 GMT  
		Size: 5.5 MB (5545870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c63ae71f01c59759e3396b7531bbb79d6964dccbda1e30320d0f40f129e4e1d4`  
		Last Modified: Wed, 14 Jan 2026 22:45:32 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1def3dc5737ea1fecb867708d6766bbeac8015b814a3fa397d84cde8b5a574b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195652360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ea675c43eb2cc01fedf882cf4e8365e77066eed73ed181b231032e049f8e1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:53:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 17:53:56 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 17:53:56 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:53:56 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:54:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:54:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:54:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:54:08 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:39:39 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:39:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:39:39 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:39:39 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:39:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:42:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:42:45 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:42:45 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:42:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:42:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:42:45 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:42:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94556139788bb73450f9a19e50325260eb3eff4a115df7a205b320c94676a6db`  
		Last Modified: Wed, 14 Jan 2026 17:54:38 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a171d6edf3b8fe4145dd3878b452a1740e88103062a31e0b83c2f5ea0c0baf34`  
		Last Modified: Wed, 14 Jan 2026 17:54:22 GMT  
		Size: 37.1 MB (37069635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a750808306c1de3e1442eb3b604596419f3625546e139266cefbeead4cfdcb`  
		Last Modified: Wed, 14 Jan 2026 17:54:21 GMT  
		Size: 1.7 MB (1712814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c98f015a95deaaa1a35e070b378ee688cba2ae435db228c28d997eb3b5a785`  
		Last Modified: Wed, 14 Jan 2026 17:54:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c91eeddc35c4c3edab0794d1c9555a6647a089fb53b291e7ede7a5ff043376`  
		Last Modified: Wed, 14 Jan 2026 18:43:29 GMT  
		Size: 1.2 MB (1214377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93138a00436818f19f5f2116948b9b043d696c98b1697b3f8fb5870e3d4f7aac`  
		Last Modified: Wed, 14 Jan 2026 18:43:30 GMT  
		Size: 11.1 MB (11131234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1194cf0373cab15da57250da8361079573dd1602ee7d8630ea49f86884512f4`  
		Last Modified: Wed, 14 Jan 2026 23:00:58 GMT  
		Size: 120.6 MB (120585851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd413595c1444c7c368d9b777efabf6226a81b3687acac08f0b3d140c8a281b`  
		Last Modified: Wed, 14 Jan 2026 18:43:29 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:7a98eea3ffbe2c35f46a88431003a5c3db940ab022e7a2ee0c6d6f23078c882a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5574531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8885d084c4b1303681e3a6ad481ff38178afea4bef4a2fa11f92d071543d68d4`

```dockerfile
```

-	Layers:
	-	`sha256:42b26631c1310e1fc3469790a75d4686b56d466de6bde00115fa03b60ba78ff8`  
		Last Modified: Wed, 14 Jan 2026 22:45:38 GMT  
		Size: 5.5 MB (5548649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55478be482cb1effa9372d7e6889b35472ed21b0a13a62bbadf657d486cf4cf7`  
		Last Modified: Wed, 14 Jan 2026 18:43:19 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:05326f3b230ebcaf16a870884ee590431bb1a29d01d8d87a09a41393a0037f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201215192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad5733d8491a9b6df26a68e8921a996719a5f0f7ba0bc27f3125c170bd6175b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 18:03:32 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 18:03:51 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:03:51 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:03:51 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:04:02 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:04:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:04:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:02 GMT
CMD ["node"]
# Wed, 14 Jan 2026 19:02:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 19:02:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 19:02:58 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 19:02:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 19:03:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 19:04:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 19:04:26 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 19:04:26 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 19:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 19:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 19:04:26 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 19:04:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf95d83bed0199eda08876836983d38feb72586a2985a0da340311e424a416e`  
		Last Modified: Wed, 14 Jan 2026 18:04:23 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2bcc6689e38d70d8b016ce5e5f9254605e5a1827fc3549cad3c7d22bcd86f7`  
		Last Modified: Wed, 14 Jan 2026 18:04:17 GMT  
		Size: 40.9 MB (40939889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb03eb22090828709af26f65e5655cf9d2aaeee32b20e995b21955aca5d2ba49`  
		Last Modified: Wed, 14 Jan 2026 18:04:24 GMT  
		Size: 1.7 MB (1712644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d1a9e57fca43837ac4707f53678b31d57e8a5ffb858b517fbe1e14e10c4fa2`  
		Last Modified: Wed, 14 Jan 2026 18:04:24 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e118ef5b835473ac21ddb690f1160b8570e55cb9729aa9dd8d193f443974d2d`  
		Last Modified: Wed, 14 Jan 2026 19:05:09 GMT  
		Size: 1.2 MB (1201468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3902afac263c59545e76f6e49a556600b4063e403906ce2f8eeaa72e85537a`  
		Last Modified: Wed, 14 Jan 2026 19:05:01 GMT  
		Size: 11.1 MB (11130555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcecace1c1d8106aee4ce164b294632123616b8550a3a7e54f6a1111530a4bea`  
		Last Modified: Wed, 14 Jan 2026 19:05:04 GMT  
		Size: 118.1 MB (118118417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7aad11f83d9940dd0d0a1041e12009f758b715c2f5eafde21d7d164af53398`  
		Last Modified: Wed, 14 Jan 2026 19:05:09 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:16084e26a1fa6ae241fbbdf34a7c3c902a5309dc6dc0212c019aca53a7db2dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5572115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7aac1bd7927737628a112a10462aa3fbc99969f77359d8d93f9884634768b6`

```dockerfile
```

-	Layers:
	-	`sha256:4e0c51f773b548f7467dbdabeb83d2c7632bf9f96fb992f954472dc6d41135c4`  
		Last Modified: Wed, 14 Jan 2026 22:46:29 GMT  
		Size: 5.5 MB (5546197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ecb1604832e3f3d243c525a79dbb88f1faf6db43c9a723654289d67fcdcd948`  
		Last Modified: Wed, 14 Jan 2026 22:46:30 GMT  
		Size: 25.9 KB (25918 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; s390x

```console
$ docker pull ghost@sha256:1cd9cf77522db40b606b005a19366d790b418c814ec945a07f3ed5dd410d96f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204846417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8808b3c6d6769e676d15a1ce727a65795133d7672f9dc5ebb45e3101f7e1d262`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 22:37:04 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 22:37:04 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 22:37:04 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 22:37:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 22:37:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 22:37:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 22:37:16 GMT
CMD ["node"]
# Thu, 15 Jan 2026 01:02:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 01:02:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 01:02:35 GMT
ENV NODE_ENV=production
# Thu, 15 Jan 2026 01:02:35 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 15 Jan 2026 01:03:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_VERSION=5.130.6
# Thu, 15 Jan 2026 01:05:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 15 Jan 2026 01:06:00 GMT
WORKDIR /var/lib/ghost
# Thu, 15 Jan 2026 01:06:00 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 15 Jan 2026 01:06:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 01:06:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 01:06:00 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 15 Jan 2026 01:06:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d139ad9a3a58767f140c3201036e062e1a612d605a2d9ad8f971d9d78b53105`  
		Last Modified: Tue, 13 Jan 2026 02:16:16 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827efbde1648435491ba62b510e28551b594939199de56cee538a1f01371cc4e`  
		Last Modified: Wed, 14 Jan 2026 22:37:49 GMT  
		Size: 41.2 MB (41235091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41b1966c4db6588397703a43f67707a24275fcaceb203375e40b0d8520037e4`  
		Last Modified: Wed, 14 Jan 2026 22:37:40 GMT  
		Size: 1.7 MB (1712672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a005686fc9589995c77fa7e3f301874174f58be05d6ce55d4d5604c9c7ec3a7`  
		Last Modified: Wed, 14 Jan 2026 22:37:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc719149c31f0c56379e9cd42770bf15660653b6f99927f5e96e24ca5594d5a9`  
		Last Modified: Thu, 15 Jan 2026 01:06:59 GMT  
		Size: 1.2 MB (1221465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1de61dc8629489d0d144e9cc3c0652ea0b45c0b60b3df3a37295b3af1ec5511`  
		Last Modified: Thu, 15 Jan 2026 01:07:01 GMT  
		Size: 11.1 MB (11130832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090b7b079c281cdfbb766e16c051dccaeb523eb6eb205315c5affd18a95083d`  
		Last Modified: Thu, 15 Jan 2026 01:07:17 GMT  
		Size: 122.7 MB (122657613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3472e72d73ac3b924f65cb42f3e7414faf9e7496284fafb1c5bf78cbab6a735a`  
		Last Modified: Thu, 15 Jan 2026 01:06:59 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:fe3968e30977cde7c01f46ff921b1389c3c9a6803f06e0d85adb6917e14fd904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5565453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef5dc2cff512b217a0faa818e5f4d1fcdc5c05278b787cc97275508a120e2dc`

```dockerfile
```

-	Layers:
	-	`sha256:5e0bcc04be75b107f4391254e47c843ff5cc050fea95760db87e2e7983eefe26`  
		Last Modified: Thu, 15 Jan 2026 01:45:32 GMT  
		Size: 5.5 MB (5539693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50838335d46938630e13acec5047d86765db6491b2c740b55ebcef9a275bf0f7`  
		Last Modified: Thu, 15 Jan 2026 01:45:33 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-alpine`

```console
$ docker pull ghost@sha256:b47bab950421229f3eb26fb9630f2780c333258b8e83832eecac5a7b6459f8ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:5c6a9e12a1a09210465a8f6e8a385f3923594a289221ed2367ec1b0bf25ceb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175688282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7da2cb090fcdf1209095ba1a3061995503245e5e403efe4461e1c9bb63f2a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:59:23 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 17:59:23 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:23 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:59:26 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:59:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:59:26 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:18:31 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 14 Jan 2026 18:18:33 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:18:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:18:33 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:18:33 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:18:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:19:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:19:34 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:19:34 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:19:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:19:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:19:34 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:19:34 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b4197efb6ccd7f8b482ae7800f1c9c78c044ea192587887300080bcff6b2c9`  
		Last Modified: Wed, 14 Jan 2026 17:59:46 GMT  
		Size: 42.8 MB (42782546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcec91425079e7b455efc5f2a18d026450c47c9382c41897620afc6b1424e44`  
		Last Modified: Wed, 14 Jan 2026 17:59:42 GMT  
		Size: 1.3 MB (1262125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b3afaea3b1b1ab04a268431e10dcace7883019a5da7d326aa35dc9713fcbb5`  
		Last Modified: Wed, 14 Jan 2026 17:59:43 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7f70a9ff0123d9c3d9eb6573cea8a3db09aa67876ef91309c6d49b24832f8`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 821.9 KB (821897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce01720e64ebc3c598a94cf7ab8a0b8426ed906cad36275ce2bafb9f9e9ef93`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 928.3 KB (928321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddde8b324021195ae3902763179e8779b5746f899505e8adbf65ec8a5da0493`  
		Last Modified: Wed, 14 Jan 2026 18:20:13 GMT  
		Size: 11.1 MB (11127580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0ff6b45f57d4aac775d5146addfedfcb6298f7973eaa0a33d4c1a4e849048f`  
		Last Modified: Wed, 14 Jan 2026 18:20:06 GMT  
		Size: 114.9 MB (114904690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c7e090fd4daa34bb8674ddb1eee416ae8ea4a523c13c702c0737c1190da833`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:213b51088fb0d2bd0535615ad04851e8d6d5f6caf9c6057a322807c93211bca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cd647d6bb7c04172e5eb7d7f7f108ceb35ebc8cc0c7ac9ee71a479c09f768c`

```dockerfile
```

-	Layers:
	-	`sha256:f2c55d77a15b35ffa5b32acab8ad55597ad56cbf005a2cf9e76ea13eb024637e`  
		Last Modified: Wed, 14 Jan 2026 22:45:41 GMT  
		Size: 3.3 MB (3333865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17a5891a3ddc6a8ca2c22c2aa06d3f913ca91d36e68452fc60ec5323afb4643`  
		Last Modified: Wed, 14 Jan 2026 22:45:41 GMT  
		Size: 25.8 KB (25794 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:79d0336eb76db7012757d0b0c678806f5669222da636047e591d0e0dfcd66653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186902852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbfecc00b666b69dd0085b71520e9433c0e643811d19246d9f25c46c470060d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:23:11 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:23:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:23:11 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:23:14 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:23:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:23:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:23:14 GMT
CMD ["node"]
# Wed, 14 Jan 2026 19:53:58 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 14 Jan 2026 19:54:00 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 19:54:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 19:54:00 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 19:54:00 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 19:54:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 19:55:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 19:55:35 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 19:55:35 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 19:55:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 19:55:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 19:55:35 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 19:55:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc83bacf48e781625d7de46541986e8525b67c1b1644803b5ff90d4ad73425c`  
		Last Modified: Wed, 14 Jan 2026 18:23:40 GMT  
		Size: 43.1 MB (43121294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d6ffd8958149c983c185c5a62d19cba7ee8807466e60c7993d78a2867eef11`  
		Last Modified: Wed, 14 Jan 2026 18:23:28 GMT  
		Size: 1.3 MB (1262980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e74b1344e24146a5181cea893d6035d8d412a89b8374e4d4360f6c35d985760`  
		Last Modified: Wed, 14 Jan 2026 18:23:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08480380b471ead2ef68b300d726de122f4578af161a7480be222a8cb93a106d`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 891.3 KB (891298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72fa1b9ceca0f979177321cf501516a7bff15507488a496f6716cf690c5d479`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 881.3 KB (881271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc99bbd104c815f9206ba50c4d163ca7add064ca0168235e27491a53b9e875`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 11.1 MB (11130917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99813db7ad424bd85f8f1a588a3de54353c3e5fbf21fd18e5ffc652b1cd108bc`  
		Last Modified: Wed, 14 Jan 2026 19:56:37 GMT  
		Size: 125.4 MB (125418338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f96912e44f74eef53e2f59c6c945e7e536a04cc10c8efad7463cbafcd8efcf4`  
		Last Modified: Wed, 14 Jan 2026 19:56:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c4e617af1b7cd29cf18eebe8ff6c19db72a31a665efe84e24026956edbbc4a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf87615f8009178f1b9e93b65d43b4ae98eec19f547cdfa1e0b3a696d166d6ec`

```dockerfile
```

-	Layers:
	-	`sha256:98253e904a7ceda72e185567f6497298699d8bea0b4c2edd33ad75cef5b7ce3b`  
		Last Modified: Wed, 14 Jan 2026 22:45:46 GMT  
		Size: 3.3 MB (3333347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21bc5d960e204ac6d2cb27314f9831276fcba3ba4d61c55097a88e788f10de5a`  
		Last Modified: Wed, 14 Jan 2026 19:56:09 GMT  
		Size: 26.0 KB (25966 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-alpine3.23`

```console
$ docker pull ghost@sha256:b47bab950421229f3eb26fb9630f2780c333258b8e83832eecac5a7b6459f8ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:5c6a9e12a1a09210465a8f6e8a385f3923594a289221ed2367ec1b0bf25ceb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175688282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7da2cb090fcdf1209095ba1a3061995503245e5e403efe4461e1c9bb63f2a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:59:23 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 17:59:23 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:23 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:59:26 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:59:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:59:26 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:18:31 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 14 Jan 2026 18:18:33 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:18:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:18:33 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:18:33 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:18:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:19:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:19:34 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:19:34 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:19:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:19:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:19:34 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:19:34 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b4197efb6ccd7f8b482ae7800f1c9c78c044ea192587887300080bcff6b2c9`  
		Last Modified: Wed, 14 Jan 2026 17:59:46 GMT  
		Size: 42.8 MB (42782546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcec91425079e7b455efc5f2a18d026450c47c9382c41897620afc6b1424e44`  
		Last Modified: Wed, 14 Jan 2026 17:59:42 GMT  
		Size: 1.3 MB (1262125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b3afaea3b1b1ab04a268431e10dcace7883019a5da7d326aa35dc9713fcbb5`  
		Last Modified: Wed, 14 Jan 2026 17:59:43 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7f70a9ff0123d9c3d9eb6573cea8a3db09aa67876ef91309c6d49b24832f8`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 821.9 KB (821897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce01720e64ebc3c598a94cf7ab8a0b8426ed906cad36275ce2bafb9f9e9ef93`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 928.3 KB (928321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddde8b324021195ae3902763179e8779b5746f899505e8adbf65ec8a5da0493`  
		Last Modified: Wed, 14 Jan 2026 18:20:13 GMT  
		Size: 11.1 MB (11127580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0ff6b45f57d4aac775d5146addfedfcb6298f7973eaa0a33d4c1a4e849048f`  
		Last Modified: Wed, 14 Jan 2026 18:20:06 GMT  
		Size: 114.9 MB (114904690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c7e090fd4daa34bb8674ddb1eee416ae8ea4a523c13c702c0737c1190da833`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:213b51088fb0d2bd0535615ad04851e8d6d5f6caf9c6057a322807c93211bca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cd647d6bb7c04172e5eb7d7f7f108ceb35ebc8cc0c7ac9ee71a479c09f768c`

```dockerfile
```

-	Layers:
	-	`sha256:f2c55d77a15b35ffa5b32acab8ad55597ad56cbf005a2cf9e76ea13eb024637e`  
		Last Modified: Wed, 14 Jan 2026 22:45:41 GMT  
		Size: 3.3 MB (3333865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17a5891a3ddc6a8ca2c22c2aa06d3f913ca91d36e68452fc60ec5323afb4643`  
		Last Modified: Wed, 14 Jan 2026 22:45:41 GMT  
		Size: 25.8 KB (25794 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:79d0336eb76db7012757d0b0c678806f5669222da636047e591d0e0dfcd66653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186902852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbfecc00b666b69dd0085b71520e9433c0e643811d19246d9f25c46c470060d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:23:11 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:23:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:23:11 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:23:14 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:23:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:23:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:23:14 GMT
CMD ["node"]
# Wed, 14 Jan 2026 19:53:58 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 14 Jan 2026 19:54:00 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 19:54:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 19:54:00 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 19:54:00 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 19:54:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 19:55:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 19:55:35 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 19:55:35 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 19:55:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 19:55:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 19:55:35 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 19:55:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc83bacf48e781625d7de46541986e8525b67c1b1644803b5ff90d4ad73425c`  
		Last Modified: Wed, 14 Jan 2026 18:23:40 GMT  
		Size: 43.1 MB (43121294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d6ffd8958149c983c185c5a62d19cba7ee8807466e60c7993d78a2867eef11`  
		Last Modified: Wed, 14 Jan 2026 18:23:28 GMT  
		Size: 1.3 MB (1262980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e74b1344e24146a5181cea893d6035d8d412a89b8374e4d4360f6c35d985760`  
		Last Modified: Wed, 14 Jan 2026 18:23:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08480380b471ead2ef68b300d726de122f4578af161a7480be222a8cb93a106d`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 891.3 KB (891298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72fa1b9ceca0f979177321cf501516a7bff15507488a496f6716cf690c5d479`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 881.3 KB (881271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc99bbd104c815f9206ba50c4d163ca7add064ca0168235e27491a53b9e875`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 11.1 MB (11130917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99813db7ad424bd85f8f1a588a3de54353c3e5fbf21fd18e5ffc652b1cd108bc`  
		Last Modified: Wed, 14 Jan 2026 19:56:37 GMT  
		Size: 125.4 MB (125418338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f96912e44f74eef53e2f59c6c945e7e536a04cc10c8efad7463cbafcd8efcf4`  
		Last Modified: Wed, 14 Jan 2026 19:56:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:c4e617af1b7cd29cf18eebe8ff6c19db72a31a665efe84e24026956edbbc4a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf87615f8009178f1b9e93b65d43b4ae98eec19f547cdfa1e0b3a696d166d6ec`

```dockerfile
```

-	Layers:
	-	`sha256:98253e904a7ceda72e185567f6497298699d8bea0b4c2edd33ad75cef5b7ce3b`  
		Last Modified: Wed, 14 Jan 2026 22:45:46 GMT  
		Size: 3.3 MB (3333347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21bc5d960e204ac6d2cb27314f9831276fcba3ba4d61c55097a88e788f10de5a`  
		Last Modified: Wed, 14 Jan 2026 19:56:09 GMT  
		Size: 26.0 KB (25966 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-bookworm`

```console
$ docker pull ghost@sha256:febc30a0a2dd702d9c625c76ce06c623e863ddf4adc225207a9f6a7983af2f1f
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
$ docker pull ghost@sha256:cd75c4c53872d65e5ad4aa0192ff7e06ffb838d6e9c3da32c377d67c9638c2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201329353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a261a521c9c9852b5853931a719ef8fee44d5eae6cd9443756a46de2e0d6b4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:59:41 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 18:00:00 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:00:00 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:00:00 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:00:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:00:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:00:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:00:12 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:18:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:18:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:18:03 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:18:03 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:18:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:19:21 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:19:22 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:19:22 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:19:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:19:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:19:22 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:19:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b9523dc7f8055cf2750f04c65434cae8f1b05241e73a5f0878d117366ad8a`  
		Last Modified: Wed, 14 Jan 2026 18:00:26 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe53019ce11f9bf83b30d24ab04d6dc4aa05dedf8c520e04da0559608edeade`  
		Last Modified: Wed, 14 Jan 2026 18:00:41 GMT  
		Size: 41.0 MB (40982889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98168ca575a7f9a177a9348c0ff4ed8e5c9ca39eb648a0654dd3c29928412cf`  
		Last Modified: Wed, 14 Jan 2026 18:00:36 GMT  
		Size: 1.7 MB (1712658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d393bf487b04ce90e509f8c13715578b3c9785f7aa2ba9bcd797b5a50c0e731`  
		Last Modified: Wed, 14 Jan 2026 18:00:36 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702e15ae043f817422edb4562290d19f8e3c32af780cb10a7b282c3fbfd33229`  
		Last Modified: Wed, 14 Jan 2026 18:19:54 GMT  
		Size: 1.2 MB (1247526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc785f759f72294cb94bba72eb544eae8fa9089e1b63e84617c4734a350ae3fc`  
		Last Modified: Wed, 14 Jan 2026 18:20:07 GMT  
		Size: 11.1 MB (11130104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a230df14864bc5e101a75973ad2d959247bef61a75d16c7dbe67434e4e797827`  
		Last Modified: Wed, 14 Jan 2026 18:20:21 GMT  
		Size: 118.0 MB (118023275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9727a9a33d14a10eaaa91e3ef41ef973e897614d2baf36d19cd5e6c52ec75`  
		Last Modified: Wed, 14 Jan 2026 18:20:05 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:fefa43decb4bf4f70e892fdb14ec6e62534005addeec7d877b8e1861ffc0afa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c342ab01f17491e38b2185ce253fe064b56729fe4445f5d94e627c3203d85e1d`

```dockerfile
```

-	Layers:
	-	`sha256:c6da51f12795fa5fa6b7125e01ed6e0814c53906dd20709c03421507b5c72c13`  
		Last Modified: Wed, 14 Jan 2026 22:45:31 GMT  
		Size: 5.5 MB (5545870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c63ae71f01c59759e3396b7531bbb79d6964dccbda1e30320d0f40f129e4e1d4`  
		Last Modified: Wed, 14 Jan 2026 22:45:32 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1def3dc5737ea1fecb867708d6766bbeac8015b814a3fa397d84cde8b5a574b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195652360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ea675c43eb2cc01fedf882cf4e8365e77066eed73ed181b231032e049f8e1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:53:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 17:53:56 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 17:53:56 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:53:56 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:54:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:54:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:54:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:54:08 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:39:39 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:39:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:39:39 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:39:39 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:39:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:42:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:42:45 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:42:45 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:42:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:42:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:42:45 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:42:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94556139788bb73450f9a19e50325260eb3eff4a115df7a205b320c94676a6db`  
		Last Modified: Wed, 14 Jan 2026 17:54:38 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a171d6edf3b8fe4145dd3878b452a1740e88103062a31e0b83c2f5ea0c0baf34`  
		Last Modified: Wed, 14 Jan 2026 17:54:22 GMT  
		Size: 37.1 MB (37069635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a750808306c1de3e1442eb3b604596419f3625546e139266cefbeead4cfdcb`  
		Last Modified: Wed, 14 Jan 2026 17:54:21 GMT  
		Size: 1.7 MB (1712814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c98f015a95deaaa1a35e070b378ee688cba2ae435db228c28d997eb3b5a785`  
		Last Modified: Wed, 14 Jan 2026 17:54:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c91eeddc35c4c3edab0794d1c9555a6647a089fb53b291e7ede7a5ff043376`  
		Last Modified: Wed, 14 Jan 2026 18:43:29 GMT  
		Size: 1.2 MB (1214377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93138a00436818f19f5f2116948b9b043d696c98b1697b3f8fb5870e3d4f7aac`  
		Last Modified: Wed, 14 Jan 2026 18:43:30 GMT  
		Size: 11.1 MB (11131234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1194cf0373cab15da57250da8361079573dd1602ee7d8630ea49f86884512f4`  
		Last Modified: Wed, 14 Jan 2026 23:00:58 GMT  
		Size: 120.6 MB (120585851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd413595c1444c7c368d9b777efabf6226a81b3687acac08f0b3d140c8a281b`  
		Last Modified: Wed, 14 Jan 2026 18:43:29 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:7a98eea3ffbe2c35f46a88431003a5c3db940ab022e7a2ee0c6d6f23078c882a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5574531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8885d084c4b1303681e3a6ad481ff38178afea4bef4a2fa11f92d071543d68d4`

```dockerfile
```

-	Layers:
	-	`sha256:42b26631c1310e1fc3469790a75d4686b56d466de6bde00115fa03b60ba78ff8`  
		Last Modified: Wed, 14 Jan 2026 22:45:38 GMT  
		Size: 5.5 MB (5548649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55478be482cb1effa9372d7e6889b35472ed21b0a13a62bbadf657d486cf4cf7`  
		Last Modified: Wed, 14 Jan 2026 18:43:19 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:05326f3b230ebcaf16a870884ee590431bb1a29d01d8d87a09a41393a0037f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201215192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad5733d8491a9b6df26a68e8921a996719a5f0f7ba0bc27f3125c170bd6175b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 18:03:32 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 18:03:51 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:03:51 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:03:51 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:04:02 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:04:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:04:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:02 GMT
CMD ["node"]
# Wed, 14 Jan 2026 19:02:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 19:02:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 19:02:58 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 19:02:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 19:03:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 19:04:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 19:04:26 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 19:04:26 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 19:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 19:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 19:04:26 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 19:04:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf95d83bed0199eda08876836983d38feb72586a2985a0da340311e424a416e`  
		Last Modified: Wed, 14 Jan 2026 18:04:23 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2bcc6689e38d70d8b016ce5e5f9254605e5a1827fc3549cad3c7d22bcd86f7`  
		Last Modified: Wed, 14 Jan 2026 18:04:17 GMT  
		Size: 40.9 MB (40939889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb03eb22090828709af26f65e5655cf9d2aaeee32b20e995b21955aca5d2ba49`  
		Last Modified: Wed, 14 Jan 2026 18:04:24 GMT  
		Size: 1.7 MB (1712644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d1a9e57fca43837ac4707f53678b31d57e8a5ffb858b517fbe1e14e10c4fa2`  
		Last Modified: Wed, 14 Jan 2026 18:04:24 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e118ef5b835473ac21ddb690f1160b8570e55cb9729aa9dd8d193f443974d2d`  
		Last Modified: Wed, 14 Jan 2026 19:05:09 GMT  
		Size: 1.2 MB (1201468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3902afac263c59545e76f6e49a556600b4063e403906ce2f8eeaa72e85537a`  
		Last Modified: Wed, 14 Jan 2026 19:05:01 GMT  
		Size: 11.1 MB (11130555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcecace1c1d8106aee4ce164b294632123616b8550a3a7e54f6a1111530a4bea`  
		Last Modified: Wed, 14 Jan 2026 19:05:04 GMT  
		Size: 118.1 MB (118118417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7aad11f83d9940dd0d0a1041e12009f758b715c2f5eafde21d7d164af53398`  
		Last Modified: Wed, 14 Jan 2026 19:05:09 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:16084e26a1fa6ae241fbbdf34a7c3c902a5309dc6dc0212c019aca53a7db2dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5572115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7aac1bd7927737628a112a10462aa3fbc99969f77359d8d93f9884634768b6`

```dockerfile
```

-	Layers:
	-	`sha256:4e0c51f773b548f7467dbdabeb83d2c7632bf9f96fb992f954472dc6d41135c4`  
		Last Modified: Wed, 14 Jan 2026 22:46:29 GMT  
		Size: 5.5 MB (5546197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ecb1604832e3f3d243c525a79dbb88f1faf6db43c9a723654289d67fcdcd948`  
		Last Modified: Wed, 14 Jan 2026 22:46:30 GMT  
		Size: 25.9 KB (25918 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:1cd9cf77522db40b606b005a19366d790b418c814ec945a07f3ed5dd410d96f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204846417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8808b3c6d6769e676d15a1ce727a65795133d7672f9dc5ebb45e3101f7e1d262`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 22:37:04 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 22:37:04 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 22:37:04 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 22:37:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 22:37:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 22:37:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 22:37:16 GMT
CMD ["node"]
# Thu, 15 Jan 2026 01:02:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 01:02:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 01:02:35 GMT
ENV NODE_ENV=production
# Thu, 15 Jan 2026 01:02:35 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 15 Jan 2026 01:03:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_VERSION=5.130.6
# Thu, 15 Jan 2026 01:05:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 15 Jan 2026 01:06:00 GMT
WORKDIR /var/lib/ghost
# Thu, 15 Jan 2026 01:06:00 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 15 Jan 2026 01:06:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 01:06:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 01:06:00 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 15 Jan 2026 01:06:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d139ad9a3a58767f140c3201036e062e1a612d605a2d9ad8f971d9d78b53105`  
		Last Modified: Tue, 13 Jan 2026 02:16:16 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827efbde1648435491ba62b510e28551b594939199de56cee538a1f01371cc4e`  
		Last Modified: Wed, 14 Jan 2026 22:37:49 GMT  
		Size: 41.2 MB (41235091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41b1966c4db6588397703a43f67707a24275fcaceb203375e40b0d8520037e4`  
		Last Modified: Wed, 14 Jan 2026 22:37:40 GMT  
		Size: 1.7 MB (1712672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a005686fc9589995c77fa7e3f301874174f58be05d6ce55d4d5604c9c7ec3a7`  
		Last Modified: Wed, 14 Jan 2026 22:37:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc719149c31f0c56379e9cd42770bf15660653b6f99927f5e96e24ca5594d5a9`  
		Last Modified: Thu, 15 Jan 2026 01:06:59 GMT  
		Size: 1.2 MB (1221465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1de61dc8629489d0d144e9cc3c0652ea0b45c0b60b3df3a37295b3af1ec5511`  
		Last Modified: Thu, 15 Jan 2026 01:07:01 GMT  
		Size: 11.1 MB (11130832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090b7b079c281cdfbb766e16c051dccaeb523eb6eb205315c5affd18a95083d`  
		Last Modified: Thu, 15 Jan 2026 01:07:17 GMT  
		Size: 122.7 MB (122657613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3472e72d73ac3b924f65cb42f3e7414faf9e7496284fafb1c5bf78cbab6a735a`  
		Last Modified: Thu, 15 Jan 2026 01:06:59 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:fe3968e30977cde7c01f46ff921b1389c3c9a6803f06e0d85adb6917e14fd904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5565453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef5dc2cff512b217a0faa818e5f4d1fcdc5c05278b787cc97275508a120e2dc`

```dockerfile
```

-	Layers:
	-	`sha256:5e0bcc04be75b107f4391254e47c843ff5cc050fea95760db87e2e7983eefe26`  
		Last Modified: Thu, 15 Jan 2026 01:45:32 GMT  
		Size: 5.5 MB (5539693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50838335d46938630e13acec5047d86765db6491b2c740b55ebcef9a275bf0f7`  
		Last Modified: Thu, 15 Jan 2026 01:45:33 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130`

```console
$ docker pull ghost@sha256:febc30a0a2dd702d9c625c76ce06c623e863ddf4adc225207a9f6a7983af2f1f
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
$ docker pull ghost@sha256:cd75c4c53872d65e5ad4aa0192ff7e06ffb838d6e9c3da32c377d67c9638c2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201329353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a261a521c9c9852b5853931a719ef8fee44d5eae6cd9443756a46de2e0d6b4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:59:41 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 18:00:00 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:00:00 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:00:00 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:00:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:00:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:00:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:00:12 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:18:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:18:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:18:03 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:18:03 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:18:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:19:21 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:19:22 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:19:22 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:19:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:19:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:19:22 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:19:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b9523dc7f8055cf2750f04c65434cae8f1b05241e73a5f0878d117366ad8a`  
		Last Modified: Wed, 14 Jan 2026 18:00:26 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe53019ce11f9bf83b30d24ab04d6dc4aa05dedf8c520e04da0559608edeade`  
		Last Modified: Wed, 14 Jan 2026 18:00:41 GMT  
		Size: 41.0 MB (40982889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98168ca575a7f9a177a9348c0ff4ed8e5c9ca39eb648a0654dd3c29928412cf`  
		Last Modified: Wed, 14 Jan 2026 18:00:36 GMT  
		Size: 1.7 MB (1712658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d393bf487b04ce90e509f8c13715578b3c9785f7aa2ba9bcd797b5a50c0e731`  
		Last Modified: Wed, 14 Jan 2026 18:00:36 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702e15ae043f817422edb4562290d19f8e3c32af780cb10a7b282c3fbfd33229`  
		Last Modified: Wed, 14 Jan 2026 18:19:54 GMT  
		Size: 1.2 MB (1247526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc785f759f72294cb94bba72eb544eae8fa9089e1b63e84617c4734a350ae3fc`  
		Last Modified: Wed, 14 Jan 2026 18:20:07 GMT  
		Size: 11.1 MB (11130104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a230df14864bc5e101a75973ad2d959247bef61a75d16c7dbe67434e4e797827`  
		Last Modified: Wed, 14 Jan 2026 18:20:21 GMT  
		Size: 118.0 MB (118023275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9727a9a33d14a10eaaa91e3ef41ef973e897614d2baf36d19cd5e6c52ec75`  
		Last Modified: Wed, 14 Jan 2026 18:20:05 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:fefa43decb4bf4f70e892fdb14ec6e62534005addeec7d877b8e1861ffc0afa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c342ab01f17491e38b2185ce253fe064b56729fe4445f5d94e627c3203d85e1d`

```dockerfile
```

-	Layers:
	-	`sha256:c6da51f12795fa5fa6b7125e01ed6e0814c53906dd20709c03421507b5c72c13`  
		Last Modified: Wed, 14 Jan 2026 22:45:31 GMT  
		Size: 5.5 MB (5545870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c63ae71f01c59759e3396b7531bbb79d6964dccbda1e30320d0f40f129e4e1d4`  
		Last Modified: Wed, 14 Jan 2026 22:45:32 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1def3dc5737ea1fecb867708d6766bbeac8015b814a3fa397d84cde8b5a574b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195652360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ea675c43eb2cc01fedf882cf4e8365e77066eed73ed181b231032e049f8e1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:53:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 17:53:56 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 17:53:56 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:53:56 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:54:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:54:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:54:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:54:08 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:39:39 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:39:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:39:39 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:39:39 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:39:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:42:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:42:45 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:42:45 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:42:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:42:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:42:45 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:42:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94556139788bb73450f9a19e50325260eb3eff4a115df7a205b320c94676a6db`  
		Last Modified: Wed, 14 Jan 2026 17:54:38 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a171d6edf3b8fe4145dd3878b452a1740e88103062a31e0b83c2f5ea0c0baf34`  
		Last Modified: Wed, 14 Jan 2026 17:54:22 GMT  
		Size: 37.1 MB (37069635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a750808306c1de3e1442eb3b604596419f3625546e139266cefbeead4cfdcb`  
		Last Modified: Wed, 14 Jan 2026 17:54:21 GMT  
		Size: 1.7 MB (1712814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c98f015a95deaaa1a35e070b378ee688cba2ae435db228c28d997eb3b5a785`  
		Last Modified: Wed, 14 Jan 2026 17:54:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c91eeddc35c4c3edab0794d1c9555a6647a089fb53b291e7ede7a5ff043376`  
		Last Modified: Wed, 14 Jan 2026 18:43:29 GMT  
		Size: 1.2 MB (1214377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93138a00436818f19f5f2116948b9b043d696c98b1697b3f8fb5870e3d4f7aac`  
		Last Modified: Wed, 14 Jan 2026 18:43:30 GMT  
		Size: 11.1 MB (11131234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1194cf0373cab15da57250da8361079573dd1602ee7d8630ea49f86884512f4`  
		Last Modified: Wed, 14 Jan 2026 23:00:58 GMT  
		Size: 120.6 MB (120585851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd413595c1444c7c368d9b777efabf6226a81b3687acac08f0b3d140c8a281b`  
		Last Modified: Wed, 14 Jan 2026 18:43:29 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:7a98eea3ffbe2c35f46a88431003a5c3db940ab022e7a2ee0c6d6f23078c882a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5574531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8885d084c4b1303681e3a6ad481ff38178afea4bef4a2fa11f92d071543d68d4`

```dockerfile
```

-	Layers:
	-	`sha256:42b26631c1310e1fc3469790a75d4686b56d466de6bde00115fa03b60ba78ff8`  
		Last Modified: Wed, 14 Jan 2026 22:45:38 GMT  
		Size: 5.5 MB (5548649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55478be482cb1effa9372d7e6889b35472ed21b0a13a62bbadf657d486cf4cf7`  
		Last Modified: Wed, 14 Jan 2026 18:43:19 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:05326f3b230ebcaf16a870884ee590431bb1a29d01d8d87a09a41393a0037f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201215192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad5733d8491a9b6df26a68e8921a996719a5f0f7ba0bc27f3125c170bd6175b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 18:03:32 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 18:03:51 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:03:51 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:03:51 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:04:02 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:04:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:04:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:02 GMT
CMD ["node"]
# Wed, 14 Jan 2026 19:02:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 19:02:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 19:02:58 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 19:02:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 19:03:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 19:04:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 19:04:26 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 19:04:26 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 19:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 19:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 19:04:26 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 19:04:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf95d83bed0199eda08876836983d38feb72586a2985a0da340311e424a416e`  
		Last Modified: Wed, 14 Jan 2026 18:04:23 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2bcc6689e38d70d8b016ce5e5f9254605e5a1827fc3549cad3c7d22bcd86f7`  
		Last Modified: Wed, 14 Jan 2026 18:04:17 GMT  
		Size: 40.9 MB (40939889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb03eb22090828709af26f65e5655cf9d2aaeee32b20e995b21955aca5d2ba49`  
		Last Modified: Wed, 14 Jan 2026 18:04:24 GMT  
		Size: 1.7 MB (1712644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d1a9e57fca43837ac4707f53678b31d57e8a5ffb858b517fbe1e14e10c4fa2`  
		Last Modified: Wed, 14 Jan 2026 18:04:24 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e118ef5b835473ac21ddb690f1160b8570e55cb9729aa9dd8d193f443974d2d`  
		Last Modified: Wed, 14 Jan 2026 19:05:09 GMT  
		Size: 1.2 MB (1201468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3902afac263c59545e76f6e49a556600b4063e403906ce2f8eeaa72e85537a`  
		Last Modified: Wed, 14 Jan 2026 19:05:01 GMT  
		Size: 11.1 MB (11130555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcecace1c1d8106aee4ce164b294632123616b8550a3a7e54f6a1111530a4bea`  
		Last Modified: Wed, 14 Jan 2026 19:05:04 GMT  
		Size: 118.1 MB (118118417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7aad11f83d9940dd0d0a1041e12009f758b715c2f5eafde21d7d164af53398`  
		Last Modified: Wed, 14 Jan 2026 19:05:09 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:16084e26a1fa6ae241fbbdf34a7c3c902a5309dc6dc0212c019aca53a7db2dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5572115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7aac1bd7927737628a112a10462aa3fbc99969f77359d8d93f9884634768b6`

```dockerfile
```

-	Layers:
	-	`sha256:4e0c51f773b548f7467dbdabeb83d2c7632bf9f96fb992f954472dc6d41135c4`  
		Last Modified: Wed, 14 Jan 2026 22:46:29 GMT  
		Size: 5.5 MB (5546197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ecb1604832e3f3d243c525a79dbb88f1faf6db43c9a723654289d67fcdcd948`  
		Last Modified: Wed, 14 Jan 2026 22:46:30 GMT  
		Size: 25.9 KB (25918 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; s390x

```console
$ docker pull ghost@sha256:1cd9cf77522db40b606b005a19366d790b418c814ec945a07f3ed5dd410d96f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204846417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8808b3c6d6769e676d15a1ce727a65795133d7672f9dc5ebb45e3101f7e1d262`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 22:37:04 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 22:37:04 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 22:37:04 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 22:37:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 22:37:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 22:37:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 22:37:16 GMT
CMD ["node"]
# Thu, 15 Jan 2026 01:02:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 01:02:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 01:02:35 GMT
ENV NODE_ENV=production
# Thu, 15 Jan 2026 01:02:35 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 15 Jan 2026 01:03:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_VERSION=5.130.6
# Thu, 15 Jan 2026 01:05:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 15 Jan 2026 01:06:00 GMT
WORKDIR /var/lib/ghost
# Thu, 15 Jan 2026 01:06:00 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 15 Jan 2026 01:06:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 01:06:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 01:06:00 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 15 Jan 2026 01:06:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d139ad9a3a58767f140c3201036e062e1a612d605a2d9ad8f971d9d78b53105`  
		Last Modified: Tue, 13 Jan 2026 02:16:16 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827efbde1648435491ba62b510e28551b594939199de56cee538a1f01371cc4e`  
		Last Modified: Wed, 14 Jan 2026 22:37:49 GMT  
		Size: 41.2 MB (41235091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41b1966c4db6588397703a43f67707a24275fcaceb203375e40b0d8520037e4`  
		Last Modified: Wed, 14 Jan 2026 22:37:40 GMT  
		Size: 1.7 MB (1712672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a005686fc9589995c77fa7e3f301874174f58be05d6ce55d4d5604c9c7ec3a7`  
		Last Modified: Wed, 14 Jan 2026 22:37:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc719149c31f0c56379e9cd42770bf15660653b6f99927f5e96e24ca5594d5a9`  
		Last Modified: Thu, 15 Jan 2026 01:06:59 GMT  
		Size: 1.2 MB (1221465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1de61dc8629489d0d144e9cc3c0652ea0b45c0b60b3df3a37295b3af1ec5511`  
		Last Modified: Thu, 15 Jan 2026 01:07:01 GMT  
		Size: 11.1 MB (11130832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090b7b079c281cdfbb766e16c051dccaeb523eb6eb205315c5affd18a95083d`  
		Last Modified: Thu, 15 Jan 2026 01:07:17 GMT  
		Size: 122.7 MB (122657613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3472e72d73ac3b924f65cb42f3e7414faf9e7496284fafb1c5bf78cbab6a735a`  
		Last Modified: Thu, 15 Jan 2026 01:06:59 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:fe3968e30977cde7c01f46ff921b1389c3c9a6803f06e0d85adb6917e14fd904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5565453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef5dc2cff512b217a0faa818e5f4d1fcdc5c05278b787cc97275508a120e2dc`

```dockerfile
```

-	Layers:
	-	`sha256:5e0bcc04be75b107f4391254e47c843ff5cc050fea95760db87e2e7983eefe26`  
		Last Modified: Thu, 15 Jan 2026 01:45:32 GMT  
		Size: 5.5 MB (5539693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50838335d46938630e13acec5047d86765db6491b2c740b55ebcef9a275bf0f7`  
		Last Modified: Thu, 15 Jan 2026 01:45:33 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130-alpine`

```console
$ docker pull ghost@sha256:b47bab950421229f3eb26fb9630f2780c333258b8e83832eecac5a7b6459f8ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:5c6a9e12a1a09210465a8f6e8a385f3923594a289221ed2367ec1b0bf25ceb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175688282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7da2cb090fcdf1209095ba1a3061995503245e5e403efe4461e1c9bb63f2a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:59:23 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 17:59:23 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:23 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:59:26 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:59:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:59:26 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:18:31 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 14 Jan 2026 18:18:33 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:18:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:18:33 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:18:33 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:18:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:19:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:19:34 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:19:34 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:19:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:19:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:19:34 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:19:34 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b4197efb6ccd7f8b482ae7800f1c9c78c044ea192587887300080bcff6b2c9`  
		Last Modified: Wed, 14 Jan 2026 17:59:46 GMT  
		Size: 42.8 MB (42782546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcec91425079e7b455efc5f2a18d026450c47c9382c41897620afc6b1424e44`  
		Last Modified: Wed, 14 Jan 2026 17:59:42 GMT  
		Size: 1.3 MB (1262125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b3afaea3b1b1ab04a268431e10dcace7883019a5da7d326aa35dc9713fcbb5`  
		Last Modified: Wed, 14 Jan 2026 17:59:43 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7f70a9ff0123d9c3d9eb6573cea8a3db09aa67876ef91309c6d49b24832f8`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 821.9 KB (821897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce01720e64ebc3c598a94cf7ab8a0b8426ed906cad36275ce2bafb9f9e9ef93`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 928.3 KB (928321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddde8b324021195ae3902763179e8779b5746f899505e8adbf65ec8a5da0493`  
		Last Modified: Wed, 14 Jan 2026 18:20:13 GMT  
		Size: 11.1 MB (11127580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0ff6b45f57d4aac775d5146addfedfcb6298f7973eaa0a33d4c1a4e849048f`  
		Last Modified: Wed, 14 Jan 2026 18:20:06 GMT  
		Size: 114.9 MB (114904690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c7e090fd4daa34bb8674ddb1eee416ae8ea4a523c13c702c0737c1190da833`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:213b51088fb0d2bd0535615ad04851e8d6d5f6caf9c6057a322807c93211bca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cd647d6bb7c04172e5eb7d7f7f108ceb35ebc8cc0c7ac9ee71a479c09f768c`

```dockerfile
```

-	Layers:
	-	`sha256:f2c55d77a15b35ffa5b32acab8ad55597ad56cbf005a2cf9e76ea13eb024637e`  
		Last Modified: Wed, 14 Jan 2026 22:45:41 GMT  
		Size: 3.3 MB (3333865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17a5891a3ddc6a8ca2c22c2aa06d3f913ca91d36e68452fc60ec5323afb4643`  
		Last Modified: Wed, 14 Jan 2026 22:45:41 GMT  
		Size: 25.8 KB (25794 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:79d0336eb76db7012757d0b0c678806f5669222da636047e591d0e0dfcd66653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186902852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbfecc00b666b69dd0085b71520e9433c0e643811d19246d9f25c46c470060d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:23:11 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:23:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:23:11 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:23:14 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:23:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:23:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:23:14 GMT
CMD ["node"]
# Wed, 14 Jan 2026 19:53:58 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 14 Jan 2026 19:54:00 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 19:54:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 19:54:00 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 19:54:00 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 19:54:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 19:55:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 19:55:35 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 19:55:35 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 19:55:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 19:55:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 19:55:35 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 19:55:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc83bacf48e781625d7de46541986e8525b67c1b1644803b5ff90d4ad73425c`  
		Last Modified: Wed, 14 Jan 2026 18:23:40 GMT  
		Size: 43.1 MB (43121294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d6ffd8958149c983c185c5a62d19cba7ee8807466e60c7993d78a2867eef11`  
		Last Modified: Wed, 14 Jan 2026 18:23:28 GMT  
		Size: 1.3 MB (1262980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e74b1344e24146a5181cea893d6035d8d412a89b8374e4d4360f6c35d985760`  
		Last Modified: Wed, 14 Jan 2026 18:23:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08480380b471ead2ef68b300d726de122f4578af161a7480be222a8cb93a106d`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 891.3 KB (891298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72fa1b9ceca0f979177321cf501516a7bff15507488a496f6716cf690c5d479`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 881.3 KB (881271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc99bbd104c815f9206ba50c4d163ca7add064ca0168235e27491a53b9e875`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 11.1 MB (11130917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99813db7ad424bd85f8f1a588a3de54353c3e5fbf21fd18e5ffc652b1cd108bc`  
		Last Modified: Wed, 14 Jan 2026 19:56:37 GMT  
		Size: 125.4 MB (125418338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f96912e44f74eef53e2f59c6c945e7e536a04cc10c8efad7463cbafcd8efcf4`  
		Last Modified: Wed, 14 Jan 2026 19:56:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c4e617af1b7cd29cf18eebe8ff6c19db72a31a665efe84e24026956edbbc4a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf87615f8009178f1b9e93b65d43b4ae98eec19f547cdfa1e0b3a696d166d6ec`

```dockerfile
```

-	Layers:
	-	`sha256:98253e904a7ceda72e185567f6497298699d8bea0b4c2edd33ad75cef5b7ce3b`  
		Last Modified: Wed, 14 Jan 2026 22:45:46 GMT  
		Size: 3.3 MB (3333347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21bc5d960e204ac6d2cb27314f9831276fcba3ba4d61c55097a88e788f10de5a`  
		Last Modified: Wed, 14 Jan 2026 19:56:09 GMT  
		Size: 26.0 KB (25966 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130-alpine3.23`

```console
$ docker pull ghost@sha256:b47bab950421229f3eb26fb9630f2780c333258b8e83832eecac5a7b6459f8ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:5c6a9e12a1a09210465a8f6e8a385f3923594a289221ed2367ec1b0bf25ceb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175688282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7da2cb090fcdf1209095ba1a3061995503245e5e403efe4461e1c9bb63f2a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:59:23 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 17:59:23 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:23 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:59:26 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:59:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:59:26 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:18:31 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 14 Jan 2026 18:18:33 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:18:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:18:33 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:18:33 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:18:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:19:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:19:34 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:19:34 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:19:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:19:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:19:34 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:19:34 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b4197efb6ccd7f8b482ae7800f1c9c78c044ea192587887300080bcff6b2c9`  
		Last Modified: Wed, 14 Jan 2026 17:59:46 GMT  
		Size: 42.8 MB (42782546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcec91425079e7b455efc5f2a18d026450c47c9382c41897620afc6b1424e44`  
		Last Modified: Wed, 14 Jan 2026 17:59:42 GMT  
		Size: 1.3 MB (1262125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b3afaea3b1b1ab04a268431e10dcace7883019a5da7d326aa35dc9713fcbb5`  
		Last Modified: Wed, 14 Jan 2026 17:59:43 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7f70a9ff0123d9c3d9eb6573cea8a3db09aa67876ef91309c6d49b24832f8`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 821.9 KB (821897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce01720e64ebc3c598a94cf7ab8a0b8426ed906cad36275ce2bafb9f9e9ef93`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 928.3 KB (928321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddde8b324021195ae3902763179e8779b5746f899505e8adbf65ec8a5da0493`  
		Last Modified: Wed, 14 Jan 2026 18:20:13 GMT  
		Size: 11.1 MB (11127580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0ff6b45f57d4aac775d5146addfedfcb6298f7973eaa0a33d4c1a4e849048f`  
		Last Modified: Wed, 14 Jan 2026 18:20:06 GMT  
		Size: 114.9 MB (114904690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c7e090fd4daa34bb8674ddb1eee416ae8ea4a523c13c702c0737c1190da833`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:213b51088fb0d2bd0535615ad04851e8d6d5f6caf9c6057a322807c93211bca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cd647d6bb7c04172e5eb7d7f7f108ceb35ebc8cc0c7ac9ee71a479c09f768c`

```dockerfile
```

-	Layers:
	-	`sha256:f2c55d77a15b35ffa5b32acab8ad55597ad56cbf005a2cf9e76ea13eb024637e`  
		Last Modified: Wed, 14 Jan 2026 22:45:41 GMT  
		Size: 3.3 MB (3333865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17a5891a3ddc6a8ca2c22c2aa06d3f913ca91d36e68452fc60ec5323afb4643`  
		Last Modified: Wed, 14 Jan 2026 22:45:41 GMT  
		Size: 25.8 KB (25794 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:79d0336eb76db7012757d0b0c678806f5669222da636047e591d0e0dfcd66653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186902852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbfecc00b666b69dd0085b71520e9433c0e643811d19246d9f25c46c470060d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:23:11 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:23:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:23:11 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:23:14 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:23:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:23:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:23:14 GMT
CMD ["node"]
# Wed, 14 Jan 2026 19:53:58 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 14 Jan 2026 19:54:00 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 19:54:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 19:54:00 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 19:54:00 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 19:54:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 19:55:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 19:55:35 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 19:55:35 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 19:55:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 19:55:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 19:55:35 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 19:55:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc83bacf48e781625d7de46541986e8525b67c1b1644803b5ff90d4ad73425c`  
		Last Modified: Wed, 14 Jan 2026 18:23:40 GMT  
		Size: 43.1 MB (43121294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d6ffd8958149c983c185c5a62d19cba7ee8807466e60c7993d78a2867eef11`  
		Last Modified: Wed, 14 Jan 2026 18:23:28 GMT  
		Size: 1.3 MB (1262980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e74b1344e24146a5181cea893d6035d8d412a89b8374e4d4360f6c35d985760`  
		Last Modified: Wed, 14 Jan 2026 18:23:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08480380b471ead2ef68b300d726de122f4578af161a7480be222a8cb93a106d`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 891.3 KB (891298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72fa1b9ceca0f979177321cf501516a7bff15507488a496f6716cf690c5d479`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 881.3 KB (881271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc99bbd104c815f9206ba50c4d163ca7add064ca0168235e27491a53b9e875`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 11.1 MB (11130917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99813db7ad424bd85f8f1a588a3de54353c3e5fbf21fd18e5ffc652b1cd108bc`  
		Last Modified: Wed, 14 Jan 2026 19:56:37 GMT  
		Size: 125.4 MB (125418338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f96912e44f74eef53e2f59c6c945e7e536a04cc10c8efad7463cbafcd8efcf4`  
		Last Modified: Wed, 14 Jan 2026 19:56:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:c4e617af1b7cd29cf18eebe8ff6c19db72a31a665efe84e24026956edbbc4a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf87615f8009178f1b9e93b65d43b4ae98eec19f547cdfa1e0b3a696d166d6ec`

```dockerfile
```

-	Layers:
	-	`sha256:98253e904a7ceda72e185567f6497298699d8bea0b4c2edd33ad75cef5b7ce3b`  
		Last Modified: Wed, 14 Jan 2026 22:45:46 GMT  
		Size: 3.3 MB (3333347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21bc5d960e204ac6d2cb27314f9831276fcba3ba4d61c55097a88e788f10de5a`  
		Last Modified: Wed, 14 Jan 2026 19:56:09 GMT  
		Size: 26.0 KB (25966 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130-bookworm`

```console
$ docker pull ghost@sha256:febc30a0a2dd702d9c625c76ce06c623e863ddf4adc225207a9f6a7983af2f1f
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
$ docker pull ghost@sha256:cd75c4c53872d65e5ad4aa0192ff7e06ffb838d6e9c3da32c377d67c9638c2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201329353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a261a521c9c9852b5853931a719ef8fee44d5eae6cd9443756a46de2e0d6b4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:59:41 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 18:00:00 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:00:00 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:00:00 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:00:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:00:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:00:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:00:12 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:18:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:18:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:18:03 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:18:03 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:18:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:19:21 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:19:22 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:19:22 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:19:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:19:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:19:22 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:19:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b9523dc7f8055cf2750f04c65434cae8f1b05241e73a5f0878d117366ad8a`  
		Last Modified: Wed, 14 Jan 2026 18:00:26 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe53019ce11f9bf83b30d24ab04d6dc4aa05dedf8c520e04da0559608edeade`  
		Last Modified: Wed, 14 Jan 2026 18:00:41 GMT  
		Size: 41.0 MB (40982889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98168ca575a7f9a177a9348c0ff4ed8e5c9ca39eb648a0654dd3c29928412cf`  
		Last Modified: Wed, 14 Jan 2026 18:00:36 GMT  
		Size: 1.7 MB (1712658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d393bf487b04ce90e509f8c13715578b3c9785f7aa2ba9bcd797b5a50c0e731`  
		Last Modified: Wed, 14 Jan 2026 18:00:36 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702e15ae043f817422edb4562290d19f8e3c32af780cb10a7b282c3fbfd33229`  
		Last Modified: Wed, 14 Jan 2026 18:19:54 GMT  
		Size: 1.2 MB (1247526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc785f759f72294cb94bba72eb544eae8fa9089e1b63e84617c4734a350ae3fc`  
		Last Modified: Wed, 14 Jan 2026 18:20:07 GMT  
		Size: 11.1 MB (11130104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a230df14864bc5e101a75973ad2d959247bef61a75d16c7dbe67434e4e797827`  
		Last Modified: Wed, 14 Jan 2026 18:20:21 GMT  
		Size: 118.0 MB (118023275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9727a9a33d14a10eaaa91e3ef41ef973e897614d2baf36d19cd5e6c52ec75`  
		Last Modified: Wed, 14 Jan 2026 18:20:05 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:fefa43decb4bf4f70e892fdb14ec6e62534005addeec7d877b8e1861ffc0afa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c342ab01f17491e38b2185ce253fe064b56729fe4445f5d94e627c3203d85e1d`

```dockerfile
```

-	Layers:
	-	`sha256:c6da51f12795fa5fa6b7125e01ed6e0814c53906dd20709c03421507b5c72c13`  
		Last Modified: Wed, 14 Jan 2026 22:45:31 GMT  
		Size: 5.5 MB (5545870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c63ae71f01c59759e3396b7531bbb79d6964dccbda1e30320d0f40f129e4e1d4`  
		Last Modified: Wed, 14 Jan 2026 22:45:32 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1def3dc5737ea1fecb867708d6766bbeac8015b814a3fa397d84cde8b5a574b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195652360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ea675c43eb2cc01fedf882cf4e8365e77066eed73ed181b231032e049f8e1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:53:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 17:53:56 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 17:53:56 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:53:56 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:54:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:54:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:54:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:54:08 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:39:39 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:39:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:39:39 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:39:39 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:39:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:42:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:42:45 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:42:45 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:42:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:42:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:42:45 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:42:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94556139788bb73450f9a19e50325260eb3eff4a115df7a205b320c94676a6db`  
		Last Modified: Wed, 14 Jan 2026 17:54:38 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a171d6edf3b8fe4145dd3878b452a1740e88103062a31e0b83c2f5ea0c0baf34`  
		Last Modified: Wed, 14 Jan 2026 17:54:22 GMT  
		Size: 37.1 MB (37069635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a750808306c1de3e1442eb3b604596419f3625546e139266cefbeead4cfdcb`  
		Last Modified: Wed, 14 Jan 2026 17:54:21 GMT  
		Size: 1.7 MB (1712814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c98f015a95deaaa1a35e070b378ee688cba2ae435db228c28d997eb3b5a785`  
		Last Modified: Wed, 14 Jan 2026 17:54:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c91eeddc35c4c3edab0794d1c9555a6647a089fb53b291e7ede7a5ff043376`  
		Last Modified: Wed, 14 Jan 2026 18:43:29 GMT  
		Size: 1.2 MB (1214377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93138a00436818f19f5f2116948b9b043d696c98b1697b3f8fb5870e3d4f7aac`  
		Last Modified: Wed, 14 Jan 2026 18:43:30 GMT  
		Size: 11.1 MB (11131234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1194cf0373cab15da57250da8361079573dd1602ee7d8630ea49f86884512f4`  
		Last Modified: Wed, 14 Jan 2026 23:00:58 GMT  
		Size: 120.6 MB (120585851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd413595c1444c7c368d9b777efabf6226a81b3687acac08f0b3d140c8a281b`  
		Last Modified: Wed, 14 Jan 2026 18:43:29 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:7a98eea3ffbe2c35f46a88431003a5c3db940ab022e7a2ee0c6d6f23078c882a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5574531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8885d084c4b1303681e3a6ad481ff38178afea4bef4a2fa11f92d071543d68d4`

```dockerfile
```

-	Layers:
	-	`sha256:42b26631c1310e1fc3469790a75d4686b56d466de6bde00115fa03b60ba78ff8`  
		Last Modified: Wed, 14 Jan 2026 22:45:38 GMT  
		Size: 5.5 MB (5548649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55478be482cb1effa9372d7e6889b35472ed21b0a13a62bbadf657d486cf4cf7`  
		Last Modified: Wed, 14 Jan 2026 18:43:19 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:05326f3b230ebcaf16a870884ee590431bb1a29d01d8d87a09a41393a0037f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201215192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad5733d8491a9b6df26a68e8921a996719a5f0f7ba0bc27f3125c170bd6175b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 18:03:32 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 18:03:51 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:03:51 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:03:51 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:04:02 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:04:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:04:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:02 GMT
CMD ["node"]
# Wed, 14 Jan 2026 19:02:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 19:02:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 19:02:58 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 19:02:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 19:03:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 19:04:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 19:04:26 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 19:04:26 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 19:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 19:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 19:04:26 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 19:04:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf95d83bed0199eda08876836983d38feb72586a2985a0da340311e424a416e`  
		Last Modified: Wed, 14 Jan 2026 18:04:23 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2bcc6689e38d70d8b016ce5e5f9254605e5a1827fc3549cad3c7d22bcd86f7`  
		Last Modified: Wed, 14 Jan 2026 18:04:17 GMT  
		Size: 40.9 MB (40939889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb03eb22090828709af26f65e5655cf9d2aaeee32b20e995b21955aca5d2ba49`  
		Last Modified: Wed, 14 Jan 2026 18:04:24 GMT  
		Size: 1.7 MB (1712644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d1a9e57fca43837ac4707f53678b31d57e8a5ffb858b517fbe1e14e10c4fa2`  
		Last Modified: Wed, 14 Jan 2026 18:04:24 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e118ef5b835473ac21ddb690f1160b8570e55cb9729aa9dd8d193f443974d2d`  
		Last Modified: Wed, 14 Jan 2026 19:05:09 GMT  
		Size: 1.2 MB (1201468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3902afac263c59545e76f6e49a556600b4063e403906ce2f8eeaa72e85537a`  
		Last Modified: Wed, 14 Jan 2026 19:05:01 GMT  
		Size: 11.1 MB (11130555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcecace1c1d8106aee4ce164b294632123616b8550a3a7e54f6a1111530a4bea`  
		Last Modified: Wed, 14 Jan 2026 19:05:04 GMT  
		Size: 118.1 MB (118118417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7aad11f83d9940dd0d0a1041e12009f758b715c2f5eafde21d7d164af53398`  
		Last Modified: Wed, 14 Jan 2026 19:05:09 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:16084e26a1fa6ae241fbbdf34a7c3c902a5309dc6dc0212c019aca53a7db2dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5572115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7aac1bd7927737628a112a10462aa3fbc99969f77359d8d93f9884634768b6`

```dockerfile
```

-	Layers:
	-	`sha256:4e0c51f773b548f7467dbdabeb83d2c7632bf9f96fb992f954472dc6d41135c4`  
		Last Modified: Wed, 14 Jan 2026 22:46:29 GMT  
		Size: 5.5 MB (5546197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ecb1604832e3f3d243c525a79dbb88f1faf6db43c9a723654289d67fcdcd948`  
		Last Modified: Wed, 14 Jan 2026 22:46:30 GMT  
		Size: 25.9 KB (25918 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:1cd9cf77522db40b606b005a19366d790b418c814ec945a07f3ed5dd410d96f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204846417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8808b3c6d6769e676d15a1ce727a65795133d7672f9dc5ebb45e3101f7e1d262`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 22:37:04 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 22:37:04 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 22:37:04 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 22:37:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 22:37:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 22:37:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 22:37:16 GMT
CMD ["node"]
# Thu, 15 Jan 2026 01:02:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 01:02:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 01:02:35 GMT
ENV NODE_ENV=production
# Thu, 15 Jan 2026 01:02:35 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 15 Jan 2026 01:03:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_VERSION=5.130.6
# Thu, 15 Jan 2026 01:05:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 15 Jan 2026 01:06:00 GMT
WORKDIR /var/lib/ghost
# Thu, 15 Jan 2026 01:06:00 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 15 Jan 2026 01:06:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 01:06:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 01:06:00 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 15 Jan 2026 01:06:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d139ad9a3a58767f140c3201036e062e1a612d605a2d9ad8f971d9d78b53105`  
		Last Modified: Tue, 13 Jan 2026 02:16:16 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827efbde1648435491ba62b510e28551b594939199de56cee538a1f01371cc4e`  
		Last Modified: Wed, 14 Jan 2026 22:37:49 GMT  
		Size: 41.2 MB (41235091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41b1966c4db6588397703a43f67707a24275fcaceb203375e40b0d8520037e4`  
		Last Modified: Wed, 14 Jan 2026 22:37:40 GMT  
		Size: 1.7 MB (1712672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a005686fc9589995c77fa7e3f301874174f58be05d6ce55d4d5604c9c7ec3a7`  
		Last Modified: Wed, 14 Jan 2026 22:37:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc719149c31f0c56379e9cd42770bf15660653b6f99927f5e96e24ca5594d5a9`  
		Last Modified: Thu, 15 Jan 2026 01:06:59 GMT  
		Size: 1.2 MB (1221465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1de61dc8629489d0d144e9cc3c0652ea0b45c0b60b3df3a37295b3af1ec5511`  
		Last Modified: Thu, 15 Jan 2026 01:07:01 GMT  
		Size: 11.1 MB (11130832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090b7b079c281cdfbb766e16c051dccaeb523eb6eb205315c5affd18a95083d`  
		Last Modified: Thu, 15 Jan 2026 01:07:17 GMT  
		Size: 122.7 MB (122657613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3472e72d73ac3b924f65cb42f3e7414faf9e7496284fafb1c5bf78cbab6a735a`  
		Last Modified: Thu, 15 Jan 2026 01:06:59 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:fe3968e30977cde7c01f46ff921b1389c3c9a6803f06e0d85adb6917e14fd904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5565453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef5dc2cff512b217a0faa818e5f4d1fcdc5c05278b787cc97275508a120e2dc`

```dockerfile
```

-	Layers:
	-	`sha256:5e0bcc04be75b107f4391254e47c843ff5cc050fea95760db87e2e7983eefe26`  
		Last Modified: Thu, 15 Jan 2026 01:45:32 GMT  
		Size: 5.5 MB (5539693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50838335d46938630e13acec5047d86765db6491b2c740b55ebcef9a275bf0f7`  
		Last Modified: Thu, 15 Jan 2026 01:45:33 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.6`

```console
$ docker pull ghost@sha256:febc30a0a2dd702d9c625c76ce06c623e863ddf4adc225207a9f6a7983af2f1f
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

### `ghost:5.130.6` - linux; amd64

```console
$ docker pull ghost@sha256:cd75c4c53872d65e5ad4aa0192ff7e06ffb838d6e9c3da32c377d67c9638c2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201329353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a261a521c9c9852b5853931a719ef8fee44d5eae6cd9443756a46de2e0d6b4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:59:41 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 18:00:00 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:00:00 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:00:00 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:00:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:00:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:00:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:00:12 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:18:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:18:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:18:03 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:18:03 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:18:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:19:21 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:19:22 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:19:22 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:19:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:19:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:19:22 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:19:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b9523dc7f8055cf2750f04c65434cae8f1b05241e73a5f0878d117366ad8a`  
		Last Modified: Wed, 14 Jan 2026 18:00:26 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe53019ce11f9bf83b30d24ab04d6dc4aa05dedf8c520e04da0559608edeade`  
		Last Modified: Wed, 14 Jan 2026 18:00:41 GMT  
		Size: 41.0 MB (40982889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98168ca575a7f9a177a9348c0ff4ed8e5c9ca39eb648a0654dd3c29928412cf`  
		Last Modified: Wed, 14 Jan 2026 18:00:36 GMT  
		Size: 1.7 MB (1712658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d393bf487b04ce90e509f8c13715578b3c9785f7aa2ba9bcd797b5a50c0e731`  
		Last Modified: Wed, 14 Jan 2026 18:00:36 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702e15ae043f817422edb4562290d19f8e3c32af780cb10a7b282c3fbfd33229`  
		Last Modified: Wed, 14 Jan 2026 18:19:54 GMT  
		Size: 1.2 MB (1247526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc785f759f72294cb94bba72eb544eae8fa9089e1b63e84617c4734a350ae3fc`  
		Last Modified: Wed, 14 Jan 2026 18:20:07 GMT  
		Size: 11.1 MB (11130104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a230df14864bc5e101a75973ad2d959247bef61a75d16c7dbe67434e4e797827`  
		Last Modified: Wed, 14 Jan 2026 18:20:21 GMT  
		Size: 118.0 MB (118023275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9727a9a33d14a10eaaa91e3ef41ef973e897614d2baf36d19cd5e6c52ec75`  
		Last Modified: Wed, 14 Jan 2026 18:20:05 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6` - unknown; unknown

```console
$ docker pull ghost@sha256:fefa43decb4bf4f70e892fdb14ec6e62534005addeec7d877b8e1861ffc0afa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c342ab01f17491e38b2185ce253fe064b56729fe4445f5d94e627c3203d85e1d`

```dockerfile
```

-	Layers:
	-	`sha256:c6da51f12795fa5fa6b7125e01ed6e0814c53906dd20709c03421507b5c72c13`  
		Last Modified: Wed, 14 Jan 2026 22:45:31 GMT  
		Size: 5.5 MB (5545870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c63ae71f01c59759e3396b7531bbb79d6964dccbda1e30320d0f40f129e4e1d4`  
		Last Modified: Wed, 14 Jan 2026 22:45:32 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1def3dc5737ea1fecb867708d6766bbeac8015b814a3fa397d84cde8b5a574b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195652360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ea675c43eb2cc01fedf882cf4e8365e77066eed73ed181b231032e049f8e1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:53:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 17:53:56 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 17:53:56 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:53:56 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:54:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:54:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:54:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:54:08 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:39:39 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:39:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:39:39 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:39:39 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:39:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:42:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:42:45 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:42:45 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:42:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:42:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:42:45 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:42:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94556139788bb73450f9a19e50325260eb3eff4a115df7a205b320c94676a6db`  
		Last Modified: Wed, 14 Jan 2026 17:54:38 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a171d6edf3b8fe4145dd3878b452a1740e88103062a31e0b83c2f5ea0c0baf34`  
		Last Modified: Wed, 14 Jan 2026 17:54:22 GMT  
		Size: 37.1 MB (37069635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a750808306c1de3e1442eb3b604596419f3625546e139266cefbeead4cfdcb`  
		Last Modified: Wed, 14 Jan 2026 17:54:21 GMT  
		Size: 1.7 MB (1712814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c98f015a95deaaa1a35e070b378ee688cba2ae435db228c28d997eb3b5a785`  
		Last Modified: Wed, 14 Jan 2026 17:54:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c91eeddc35c4c3edab0794d1c9555a6647a089fb53b291e7ede7a5ff043376`  
		Last Modified: Wed, 14 Jan 2026 18:43:29 GMT  
		Size: 1.2 MB (1214377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93138a00436818f19f5f2116948b9b043d696c98b1697b3f8fb5870e3d4f7aac`  
		Last Modified: Wed, 14 Jan 2026 18:43:30 GMT  
		Size: 11.1 MB (11131234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1194cf0373cab15da57250da8361079573dd1602ee7d8630ea49f86884512f4`  
		Last Modified: Wed, 14 Jan 2026 23:00:58 GMT  
		Size: 120.6 MB (120585851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd413595c1444c7c368d9b777efabf6226a81b3687acac08f0b3d140c8a281b`  
		Last Modified: Wed, 14 Jan 2026 18:43:29 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6` - unknown; unknown

```console
$ docker pull ghost@sha256:7a98eea3ffbe2c35f46a88431003a5c3db940ab022e7a2ee0c6d6f23078c882a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5574531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8885d084c4b1303681e3a6ad481ff38178afea4bef4a2fa11f92d071543d68d4`

```dockerfile
```

-	Layers:
	-	`sha256:42b26631c1310e1fc3469790a75d4686b56d466de6bde00115fa03b60ba78ff8`  
		Last Modified: Wed, 14 Jan 2026 22:45:38 GMT  
		Size: 5.5 MB (5548649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55478be482cb1effa9372d7e6889b35472ed21b0a13a62bbadf657d486cf4cf7`  
		Last Modified: Wed, 14 Jan 2026 18:43:19 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:05326f3b230ebcaf16a870884ee590431bb1a29d01d8d87a09a41393a0037f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201215192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad5733d8491a9b6df26a68e8921a996719a5f0f7ba0bc27f3125c170bd6175b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 18:03:32 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 18:03:51 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:03:51 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:03:51 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:04:02 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:04:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:04:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:02 GMT
CMD ["node"]
# Wed, 14 Jan 2026 19:02:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 19:02:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 19:02:58 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 19:02:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 19:03:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 19:04:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 19:04:26 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 19:04:26 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 19:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 19:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 19:04:26 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 19:04:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf95d83bed0199eda08876836983d38feb72586a2985a0da340311e424a416e`  
		Last Modified: Wed, 14 Jan 2026 18:04:23 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2bcc6689e38d70d8b016ce5e5f9254605e5a1827fc3549cad3c7d22bcd86f7`  
		Last Modified: Wed, 14 Jan 2026 18:04:17 GMT  
		Size: 40.9 MB (40939889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb03eb22090828709af26f65e5655cf9d2aaeee32b20e995b21955aca5d2ba49`  
		Last Modified: Wed, 14 Jan 2026 18:04:24 GMT  
		Size: 1.7 MB (1712644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d1a9e57fca43837ac4707f53678b31d57e8a5ffb858b517fbe1e14e10c4fa2`  
		Last Modified: Wed, 14 Jan 2026 18:04:24 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e118ef5b835473ac21ddb690f1160b8570e55cb9729aa9dd8d193f443974d2d`  
		Last Modified: Wed, 14 Jan 2026 19:05:09 GMT  
		Size: 1.2 MB (1201468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3902afac263c59545e76f6e49a556600b4063e403906ce2f8eeaa72e85537a`  
		Last Modified: Wed, 14 Jan 2026 19:05:01 GMT  
		Size: 11.1 MB (11130555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcecace1c1d8106aee4ce164b294632123616b8550a3a7e54f6a1111530a4bea`  
		Last Modified: Wed, 14 Jan 2026 19:05:04 GMT  
		Size: 118.1 MB (118118417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7aad11f83d9940dd0d0a1041e12009f758b715c2f5eafde21d7d164af53398`  
		Last Modified: Wed, 14 Jan 2026 19:05:09 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6` - unknown; unknown

```console
$ docker pull ghost@sha256:16084e26a1fa6ae241fbbdf34a7c3c902a5309dc6dc0212c019aca53a7db2dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5572115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7aac1bd7927737628a112a10462aa3fbc99969f77359d8d93f9884634768b6`

```dockerfile
```

-	Layers:
	-	`sha256:4e0c51f773b548f7467dbdabeb83d2c7632bf9f96fb992f954472dc6d41135c4`  
		Last Modified: Wed, 14 Jan 2026 22:46:29 GMT  
		Size: 5.5 MB (5546197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ecb1604832e3f3d243c525a79dbb88f1faf6db43c9a723654289d67fcdcd948`  
		Last Modified: Wed, 14 Jan 2026 22:46:30 GMT  
		Size: 25.9 KB (25918 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6` - linux; s390x

```console
$ docker pull ghost@sha256:1cd9cf77522db40b606b005a19366d790b418c814ec945a07f3ed5dd410d96f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204846417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8808b3c6d6769e676d15a1ce727a65795133d7672f9dc5ebb45e3101f7e1d262`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 22:37:04 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 22:37:04 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 22:37:04 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 22:37:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 22:37:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 22:37:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 22:37:16 GMT
CMD ["node"]
# Thu, 15 Jan 2026 01:02:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 01:02:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 01:02:35 GMT
ENV NODE_ENV=production
# Thu, 15 Jan 2026 01:02:35 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 15 Jan 2026 01:03:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_VERSION=5.130.6
# Thu, 15 Jan 2026 01:05:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 15 Jan 2026 01:06:00 GMT
WORKDIR /var/lib/ghost
# Thu, 15 Jan 2026 01:06:00 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 15 Jan 2026 01:06:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 01:06:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 01:06:00 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 15 Jan 2026 01:06:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d139ad9a3a58767f140c3201036e062e1a612d605a2d9ad8f971d9d78b53105`  
		Last Modified: Tue, 13 Jan 2026 02:16:16 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827efbde1648435491ba62b510e28551b594939199de56cee538a1f01371cc4e`  
		Last Modified: Wed, 14 Jan 2026 22:37:49 GMT  
		Size: 41.2 MB (41235091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41b1966c4db6588397703a43f67707a24275fcaceb203375e40b0d8520037e4`  
		Last Modified: Wed, 14 Jan 2026 22:37:40 GMT  
		Size: 1.7 MB (1712672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a005686fc9589995c77fa7e3f301874174f58be05d6ce55d4d5604c9c7ec3a7`  
		Last Modified: Wed, 14 Jan 2026 22:37:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc719149c31f0c56379e9cd42770bf15660653b6f99927f5e96e24ca5594d5a9`  
		Last Modified: Thu, 15 Jan 2026 01:06:59 GMT  
		Size: 1.2 MB (1221465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1de61dc8629489d0d144e9cc3c0652ea0b45c0b60b3df3a37295b3af1ec5511`  
		Last Modified: Thu, 15 Jan 2026 01:07:01 GMT  
		Size: 11.1 MB (11130832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090b7b079c281cdfbb766e16c051dccaeb523eb6eb205315c5affd18a95083d`  
		Last Modified: Thu, 15 Jan 2026 01:07:17 GMT  
		Size: 122.7 MB (122657613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3472e72d73ac3b924f65cb42f3e7414faf9e7496284fafb1c5bf78cbab6a735a`  
		Last Modified: Thu, 15 Jan 2026 01:06:59 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6` - unknown; unknown

```console
$ docker pull ghost@sha256:fe3968e30977cde7c01f46ff921b1389c3c9a6803f06e0d85adb6917e14fd904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5565453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef5dc2cff512b217a0faa818e5f4d1fcdc5c05278b787cc97275508a120e2dc`

```dockerfile
```

-	Layers:
	-	`sha256:5e0bcc04be75b107f4391254e47c843ff5cc050fea95760db87e2e7983eefe26`  
		Last Modified: Thu, 15 Jan 2026 01:45:32 GMT  
		Size: 5.5 MB (5539693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50838335d46938630e13acec5047d86765db6491b2c740b55ebcef9a275bf0f7`  
		Last Modified: Thu, 15 Jan 2026 01:45:33 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.6-alpine`

```console
$ docker pull ghost@sha256:b47bab950421229f3eb26fb9630f2780c333258b8e83832eecac5a7b6459f8ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130.6-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:5c6a9e12a1a09210465a8f6e8a385f3923594a289221ed2367ec1b0bf25ceb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175688282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7da2cb090fcdf1209095ba1a3061995503245e5e403efe4461e1c9bb63f2a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:59:23 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 17:59:23 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:23 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:59:26 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:59:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:59:26 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:18:31 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 14 Jan 2026 18:18:33 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:18:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:18:33 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:18:33 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:18:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:19:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:19:34 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:19:34 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:19:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:19:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:19:34 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:19:34 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b4197efb6ccd7f8b482ae7800f1c9c78c044ea192587887300080bcff6b2c9`  
		Last Modified: Wed, 14 Jan 2026 17:59:46 GMT  
		Size: 42.8 MB (42782546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcec91425079e7b455efc5f2a18d026450c47c9382c41897620afc6b1424e44`  
		Last Modified: Wed, 14 Jan 2026 17:59:42 GMT  
		Size: 1.3 MB (1262125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b3afaea3b1b1ab04a268431e10dcace7883019a5da7d326aa35dc9713fcbb5`  
		Last Modified: Wed, 14 Jan 2026 17:59:43 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7f70a9ff0123d9c3d9eb6573cea8a3db09aa67876ef91309c6d49b24832f8`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 821.9 KB (821897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce01720e64ebc3c598a94cf7ab8a0b8426ed906cad36275ce2bafb9f9e9ef93`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 928.3 KB (928321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddde8b324021195ae3902763179e8779b5746f899505e8adbf65ec8a5da0493`  
		Last Modified: Wed, 14 Jan 2026 18:20:13 GMT  
		Size: 11.1 MB (11127580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0ff6b45f57d4aac775d5146addfedfcb6298f7973eaa0a33d4c1a4e849048f`  
		Last Modified: Wed, 14 Jan 2026 18:20:06 GMT  
		Size: 114.9 MB (114904690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c7e090fd4daa34bb8674ddb1eee416ae8ea4a523c13c702c0737c1190da833`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:213b51088fb0d2bd0535615ad04851e8d6d5f6caf9c6057a322807c93211bca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cd647d6bb7c04172e5eb7d7f7f108ceb35ebc8cc0c7ac9ee71a479c09f768c`

```dockerfile
```

-	Layers:
	-	`sha256:f2c55d77a15b35ffa5b32acab8ad55597ad56cbf005a2cf9e76ea13eb024637e`  
		Last Modified: Wed, 14 Jan 2026 22:45:41 GMT  
		Size: 3.3 MB (3333865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17a5891a3ddc6a8ca2c22c2aa06d3f913ca91d36e68452fc60ec5323afb4643`  
		Last Modified: Wed, 14 Jan 2026 22:45:41 GMT  
		Size: 25.8 KB (25794 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:79d0336eb76db7012757d0b0c678806f5669222da636047e591d0e0dfcd66653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186902852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbfecc00b666b69dd0085b71520e9433c0e643811d19246d9f25c46c470060d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:23:11 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:23:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:23:11 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:23:14 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:23:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:23:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:23:14 GMT
CMD ["node"]
# Wed, 14 Jan 2026 19:53:58 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 14 Jan 2026 19:54:00 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 19:54:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 19:54:00 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 19:54:00 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 19:54:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 19:55:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 19:55:35 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 19:55:35 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 19:55:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 19:55:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 19:55:35 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 19:55:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc83bacf48e781625d7de46541986e8525b67c1b1644803b5ff90d4ad73425c`  
		Last Modified: Wed, 14 Jan 2026 18:23:40 GMT  
		Size: 43.1 MB (43121294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d6ffd8958149c983c185c5a62d19cba7ee8807466e60c7993d78a2867eef11`  
		Last Modified: Wed, 14 Jan 2026 18:23:28 GMT  
		Size: 1.3 MB (1262980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e74b1344e24146a5181cea893d6035d8d412a89b8374e4d4360f6c35d985760`  
		Last Modified: Wed, 14 Jan 2026 18:23:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08480380b471ead2ef68b300d726de122f4578af161a7480be222a8cb93a106d`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 891.3 KB (891298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72fa1b9ceca0f979177321cf501516a7bff15507488a496f6716cf690c5d479`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 881.3 KB (881271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc99bbd104c815f9206ba50c4d163ca7add064ca0168235e27491a53b9e875`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 11.1 MB (11130917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99813db7ad424bd85f8f1a588a3de54353c3e5fbf21fd18e5ffc652b1cd108bc`  
		Last Modified: Wed, 14 Jan 2026 19:56:37 GMT  
		Size: 125.4 MB (125418338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f96912e44f74eef53e2f59c6c945e7e536a04cc10c8efad7463cbafcd8efcf4`  
		Last Modified: Wed, 14 Jan 2026 19:56:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c4e617af1b7cd29cf18eebe8ff6c19db72a31a665efe84e24026956edbbc4a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf87615f8009178f1b9e93b65d43b4ae98eec19f547cdfa1e0b3a696d166d6ec`

```dockerfile
```

-	Layers:
	-	`sha256:98253e904a7ceda72e185567f6497298699d8bea0b4c2edd33ad75cef5b7ce3b`  
		Last Modified: Wed, 14 Jan 2026 22:45:46 GMT  
		Size: 3.3 MB (3333347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21bc5d960e204ac6d2cb27314f9831276fcba3ba4d61c55097a88e788f10de5a`  
		Last Modified: Wed, 14 Jan 2026 19:56:09 GMT  
		Size: 26.0 KB (25966 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.6-alpine3.23`

```console
$ docker pull ghost@sha256:b47bab950421229f3eb26fb9630f2780c333258b8e83832eecac5a7b6459f8ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130.6-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:5c6a9e12a1a09210465a8f6e8a385f3923594a289221ed2367ec1b0bf25ceb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175688282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7da2cb090fcdf1209095ba1a3061995503245e5e403efe4461e1c9bb63f2a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:59:23 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 17:59:23 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:23 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:59:26 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:59:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:59:26 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:18:31 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 14 Jan 2026 18:18:33 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:18:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:18:33 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:18:33 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:18:44 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:18:44 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:19:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:19:34 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:19:34 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:19:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:19:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:19:34 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:19:34 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b4197efb6ccd7f8b482ae7800f1c9c78c044ea192587887300080bcff6b2c9`  
		Last Modified: Wed, 14 Jan 2026 17:59:46 GMT  
		Size: 42.8 MB (42782546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcec91425079e7b455efc5f2a18d026450c47c9382c41897620afc6b1424e44`  
		Last Modified: Wed, 14 Jan 2026 17:59:42 GMT  
		Size: 1.3 MB (1262125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b3afaea3b1b1ab04a268431e10dcace7883019a5da7d326aa35dc9713fcbb5`  
		Last Modified: Wed, 14 Jan 2026 17:59:43 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7f70a9ff0123d9c3d9eb6573cea8a3db09aa67876ef91309c6d49b24832f8`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 821.9 KB (821897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce01720e64ebc3c598a94cf7ab8a0b8426ed906cad36275ce2bafb9f9e9ef93`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 928.3 KB (928321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddde8b324021195ae3902763179e8779b5746f899505e8adbf65ec8a5da0493`  
		Last Modified: Wed, 14 Jan 2026 18:20:13 GMT  
		Size: 11.1 MB (11127580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0ff6b45f57d4aac775d5146addfedfcb6298f7973eaa0a33d4c1a4e849048f`  
		Last Modified: Wed, 14 Jan 2026 18:20:06 GMT  
		Size: 114.9 MB (114904690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c7e090fd4daa34bb8674ddb1eee416ae8ea4a523c13c702c0737c1190da833`  
		Last Modified: Wed, 14 Jan 2026 18:20:12 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:213b51088fb0d2bd0535615ad04851e8d6d5f6caf9c6057a322807c93211bca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cd647d6bb7c04172e5eb7d7f7f108ceb35ebc8cc0c7ac9ee71a479c09f768c`

```dockerfile
```

-	Layers:
	-	`sha256:f2c55d77a15b35ffa5b32acab8ad55597ad56cbf005a2cf9e76ea13eb024637e`  
		Last Modified: Wed, 14 Jan 2026 22:45:41 GMT  
		Size: 3.3 MB (3333865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17a5891a3ddc6a8ca2c22c2aa06d3f913ca91d36e68452fc60ec5323afb4643`  
		Last Modified: Wed, 14 Jan 2026 22:45:41 GMT  
		Size: 25.8 KB (25794 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:79d0336eb76db7012757d0b0c678806f5669222da636047e591d0e0dfcd66653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186902852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbfecc00b666b69dd0085b71520e9433c0e643811d19246d9f25c46c470060d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:23:11 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:23:11 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="c92cfcb864e84eb279f495fc2cf5de6c4877cf9f12fe5e4f21d1de5669c169ee" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:23:11 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:23:14 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:23:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:23:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:23:14 GMT
CMD ["node"]
# Wed, 14 Jan 2026 19:53:58 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 14 Jan 2026 19:54:00 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 19:54:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 19:54:00 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 19:54:00 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 19:54:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 19:54:14 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 19:55:34 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 19:55:35 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 19:55:35 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 19:55:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 19:55:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 19:55:35 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 19:55:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc83bacf48e781625d7de46541986e8525b67c1b1644803b5ff90d4ad73425c`  
		Last Modified: Wed, 14 Jan 2026 18:23:40 GMT  
		Size: 43.1 MB (43121294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d6ffd8958149c983c185c5a62d19cba7ee8807466e60c7993d78a2867eef11`  
		Last Modified: Wed, 14 Jan 2026 18:23:28 GMT  
		Size: 1.3 MB (1262980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e74b1344e24146a5181cea893d6035d8d412a89b8374e4d4360f6c35d985760`  
		Last Modified: Wed, 14 Jan 2026 18:23:34 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08480380b471ead2ef68b300d726de122f4578af161a7480be222a8cb93a106d`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 891.3 KB (891298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72fa1b9ceca0f979177321cf501516a7bff15507488a496f6716cf690c5d479`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 881.3 KB (881271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc99bbd104c815f9206ba50c4d163ca7add064ca0168235e27491a53b9e875`  
		Last Modified: Wed, 14 Jan 2026 19:56:10 GMT  
		Size: 11.1 MB (11130917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99813db7ad424bd85f8f1a588a3de54353c3e5fbf21fd18e5ffc652b1cd108bc`  
		Last Modified: Wed, 14 Jan 2026 19:56:37 GMT  
		Size: 125.4 MB (125418338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f96912e44f74eef53e2f59c6c945e7e536a04cc10c8efad7463cbafcd8efcf4`  
		Last Modified: Wed, 14 Jan 2026 19:56:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:c4e617af1b7cd29cf18eebe8ff6c19db72a31a665efe84e24026956edbbc4a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf87615f8009178f1b9e93b65d43b4ae98eec19f547cdfa1e0b3a696d166d6ec`

```dockerfile
```

-	Layers:
	-	`sha256:98253e904a7ceda72e185567f6497298699d8bea0b4c2edd33ad75cef5b7ce3b`  
		Last Modified: Wed, 14 Jan 2026 22:45:46 GMT  
		Size: 3.3 MB (3333347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21bc5d960e204ac6d2cb27314f9831276fcba3ba4d61c55097a88e788f10de5a`  
		Last Modified: Wed, 14 Jan 2026 19:56:09 GMT  
		Size: 26.0 KB (25966 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.6-bookworm`

```console
$ docker pull ghost@sha256:febc30a0a2dd702d9c625c76ce06c623e863ddf4adc225207a9f6a7983af2f1f
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

### `ghost:5.130.6-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:cd75c4c53872d65e5ad4aa0192ff7e06ffb838d6e9c3da32c377d67c9638c2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201329353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a261a521c9c9852b5853931a719ef8fee44d5eae6cd9443756a46de2e0d6b4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:59:41 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 18:00:00 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:00:00 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:00:00 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:00:12 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:00:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:00:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:00:12 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:18:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:18:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:18:03 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:18:03 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:18:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:18:14 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:19:21 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:19:22 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:19:22 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:19:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:19:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:19:22 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:19:22 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b9523dc7f8055cf2750f04c65434cae8f1b05241e73a5f0878d117366ad8a`  
		Last Modified: Wed, 14 Jan 2026 18:00:26 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe53019ce11f9bf83b30d24ab04d6dc4aa05dedf8c520e04da0559608edeade`  
		Last Modified: Wed, 14 Jan 2026 18:00:41 GMT  
		Size: 41.0 MB (40982889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98168ca575a7f9a177a9348c0ff4ed8e5c9ca39eb648a0654dd3c29928412cf`  
		Last Modified: Wed, 14 Jan 2026 18:00:36 GMT  
		Size: 1.7 MB (1712658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d393bf487b04ce90e509f8c13715578b3c9785f7aa2ba9bcd797b5a50c0e731`  
		Last Modified: Wed, 14 Jan 2026 18:00:36 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702e15ae043f817422edb4562290d19f8e3c32af780cb10a7b282c3fbfd33229`  
		Last Modified: Wed, 14 Jan 2026 18:19:54 GMT  
		Size: 1.2 MB (1247526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc785f759f72294cb94bba72eb544eae8fa9089e1b63e84617c4734a350ae3fc`  
		Last Modified: Wed, 14 Jan 2026 18:20:07 GMT  
		Size: 11.1 MB (11130104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a230df14864bc5e101a75973ad2d959247bef61a75d16c7dbe67434e4e797827`  
		Last Modified: Wed, 14 Jan 2026 18:20:21 GMT  
		Size: 118.0 MB (118023275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9727a9a33d14a10eaaa91e3ef41ef973e897614d2baf36d19cd5e6c52ec75`  
		Last Modified: Wed, 14 Jan 2026 18:20:05 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:fefa43decb4bf4f70e892fdb14ec6e62534005addeec7d877b8e1861ffc0afa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5571630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c342ab01f17491e38b2185ce253fe064b56729fe4445f5d94e627c3203d85e1d`

```dockerfile
```

-	Layers:
	-	`sha256:c6da51f12795fa5fa6b7125e01ed6e0814c53906dd20709c03421507b5c72c13`  
		Last Modified: Wed, 14 Jan 2026 22:45:31 GMT  
		Size: 5.5 MB (5545870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c63ae71f01c59759e3396b7531bbb79d6964dccbda1e30320d0f40f129e4e1d4`  
		Last Modified: Wed, 14 Jan 2026 22:45:32 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1def3dc5737ea1fecb867708d6766bbeac8015b814a3fa397d84cde8b5a574b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195652360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ea675c43eb2cc01fedf882cf4e8365e77066eed73ed181b231032e049f8e1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:53:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 17:53:56 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 17:53:56 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:53:56 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:54:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:54:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:54:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:54:08 GMT
CMD ["node"]
# Wed, 14 Jan 2026 18:39:39 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 18:39:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 18:39:39 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 18:39:39 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 18:39:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 18:39:54 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 18:42:44 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 18:42:45 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 18:42:45 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 18:42:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:42:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:42:45 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 18:42:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94556139788bb73450f9a19e50325260eb3eff4a115df7a205b320c94676a6db`  
		Last Modified: Wed, 14 Jan 2026 17:54:38 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a171d6edf3b8fe4145dd3878b452a1740e88103062a31e0b83c2f5ea0c0baf34`  
		Last Modified: Wed, 14 Jan 2026 17:54:22 GMT  
		Size: 37.1 MB (37069635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a750808306c1de3e1442eb3b604596419f3625546e139266cefbeead4cfdcb`  
		Last Modified: Wed, 14 Jan 2026 17:54:21 GMT  
		Size: 1.7 MB (1712814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c98f015a95deaaa1a35e070b378ee688cba2ae435db228c28d997eb3b5a785`  
		Last Modified: Wed, 14 Jan 2026 17:54:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c91eeddc35c4c3edab0794d1c9555a6647a089fb53b291e7ede7a5ff043376`  
		Last Modified: Wed, 14 Jan 2026 18:43:29 GMT  
		Size: 1.2 MB (1214377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93138a00436818f19f5f2116948b9b043d696c98b1697b3f8fb5870e3d4f7aac`  
		Last Modified: Wed, 14 Jan 2026 18:43:30 GMT  
		Size: 11.1 MB (11131234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1194cf0373cab15da57250da8361079573dd1602ee7d8630ea49f86884512f4`  
		Last Modified: Wed, 14 Jan 2026 23:00:58 GMT  
		Size: 120.6 MB (120585851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd413595c1444c7c368d9b777efabf6226a81b3687acac08f0b3d140c8a281b`  
		Last Modified: Wed, 14 Jan 2026 18:43:29 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:7a98eea3ffbe2c35f46a88431003a5c3db940ab022e7a2ee0c6d6f23078c882a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5574531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8885d084c4b1303681e3a6ad481ff38178afea4bef4a2fa11f92d071543d68d4`

```dockerfile
```

-	Layers:
	-	`sha256:42b26631c1310e1fc3469790a75d4686b56d466de6bde00115fa03b60ba78ff8`  
		Last Modified: Wed, 14 Jan 2026 22:45:38 GMT  
		Size: 5.5 MB (5548649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55478be482cb1effa9372d7e6889b35472ed21b0a13a62bbadf657d486cf4cf7`  
		Last Modified: Wed, 14 Jan 2026 18:43:19 GMT  
		Size: 25.9 KB (25882 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:05326f3b230ebcaf16a870884ee590431bb1a29d01d8d87a09a41393a0037f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201215192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad5733d8491a9b6df26a68e8921a996719a5f0f7ba0bc27f3125c170bd6175b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 18:03:32 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 18:03:51 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 18:03:51 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:03:51 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:04:02 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:04:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:04:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:04:02 GMT
CMD ["node"]
# Wed, 14 Jan 2026 19:02:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 19:02:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 19:02:58 GMT
ENV NODE_ENV=production
# Wed, 14 Jan 2026 19:02:58 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Wed, 14 Jan 2026 19:03:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 14 Jan 2026 19:03:12 GMT
ENV GHOST_VERSION=5.130.6
# Wed, 14 Jan 2026 19:04:25 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Wed, 14 Jan 2026 19:04:26 GMT
WORKDIR /var/lib/ghost
# Wed, 14 Jan 2026 19:04:26 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 14 Jan 2026 19:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 19:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 19:04:26 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 14 Jan 2026 19:04:26 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf95d83bed0199eda08876836983d38feb72586a2985a0da340311e424a416e`  
		Last Modified: Wed, 14 Jan 2026 18:04:23 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2bcc6689e38d70d8b016ce5e5f9254605e5a1827fc3549cad3c7d22bcd86f7`  
		Last Modified: Wed, 14 Jan 2026 18:04:17 GMT  
		Size: 40.9 MB (40939889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb03eb22090828709af26f65e5655cf9d2aaeee32b20e995b21955aca5d2ba49`  
		Last Modified: Wed, 14 Jan 2026 18:04:24 GMT  
		Size: 1.7 MB (1712644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d1a9e57fca43837ac4707f53678b31d57e8a5ffb858b517fbe1e14e10c4fa2`  
		Last Modified: Wed, 14 Jan 2026 18:04:24 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e118ef5b835473ac21ddb690f1160b8570e55cb9729aa9dd8d193f443974d2d`  
		Last Modified: Wed, 14 Jan 2026 19:05:09 GMT  
		Size: 1.2 MB (1201468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3902afac263c59545e76f6e49a556600b4063e403906ce2f8eeaa72e85537a`  
		Last Modified: Wed, 14 Jan 2026 19:05:01 GMT  
		Size: 11.1 MB (11130555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcecace1c1d8106aee4ce164b294632123616b8550a3a7e54f6a1111530a4bea`  
		Last Modified: Wed, 14 Jan 2026 19:05:04 GMT  
		Size: 118.1 MB (118118417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7aad11f83d9940dd0d0a1041e12009f758b715c2f5eafde21d7d164af53398`  
		Last Modified: Wed, 14 Jan 2026 19:05:09 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:16084e26a1fa6ae241fbbdf34a7c3c902a5309dc6dc0212c019aca53a7db2dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5572115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7aac1bd7927737628a112a10462aa3fbc99969f77359d8d93f9884634768b6`

```dockerfile
```

-	Layers:
	-	`sha256:4e0c51f773b548f7467dbdabeb83d2c7632bf9f96fb992f954472dc6d41135c4`  
		Last Modified: Wed, 14 Jan 2026 22:46:29 GMT  
		Size: 5.5 MB (5546197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ecb1604832e3f3d243c525a79dbb88f1faf6db43c9a723654289d67fcdcd948`  
		Last Modified: Wed, 14 Jan 2026 22:46:30 GMT  
		Size: 25.9 KB (25918 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.6-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:1cd9cf77522db40b606b005a19366d790b418c814ec945a07f3ed5dd410d96f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204846417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8808b3c6d6769e676d15a1ce727a65795133d7672f9dc5ebb45e3101f7e1d262`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 22:37:04 GMT
ENV NODE_VERSION=20.20.0
# Wed, 14 Jan 2026 22:37:04 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 22:37:04 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 22:37:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 22:37:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 22:37:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 22:37:16 GMT
CMD ["node"]
# Thu, 15 Jan 2026 01:02:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 01:02:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 01:02:35 GMT
ENV NODE_ENV=production
# Thu, 15 Jan 2026 01:02:35 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 15 Jan 2026 01:03:05 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Jan 2026 01:03:05 GMT
ENV GHOST_VERSION=5.130.6
# Thu, 15 Jan 2026 01:05:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Thu, 15 Jan 2026 01:06:00 GMT
WORKDIR /var/lib/ghost
# Thu, 15 Jan 2026 01:06:00 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 15 Jan 2026 01:06:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 01:06:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 01:06:00 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 15 Jan 2026 01:06:00 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d139ad9a3a58767f140c3201036e062e1a612d605a2d9ad8f971d9d78b53105`  
		Last Modified: Tue, 13 Jan 2026 02:16:16 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827efbde1648435491ba62b510e28551b594939199de56cee538a1f01371cc4e`  
		Last Modified: Wed, 14 Jan 2026 22:37:49 GMT  
		Size: 41.2 MB (41235091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41b1966c4db6588397703a43f67707a24275fcaceb203375e40b0d8520037e4`  
		Last Modified: Wed, 14 Jan 2026 22:37:40 GMT  
		Size: 1.7 MB (1712672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a005686fc9589995c77fa7e3f301874174f58be05d6ce55d4d5604c9c7ec3a7`  
		Last Modified: Wed, 14 Jan 2026 22:37:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc719149c31f0c56379e9cd42770bf15660653b6f99927f5e96e24ca5594d5a9`  
		Last Modified: Thu, 15 Jan 2026 01:06:59 GMT  
		Size: 1.2 MB (1221465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1de61dc8629489d0d144e9cc3c0652ea0b45c0b60b3df3a37295b3af1ec5511`  
		Last Modified: Thu, 15 Jan 2026 01:07:01 GMT  
		Size: 11.1 MB (11130832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090b7b079c281cdfbb766e16c051dccaeb523eb6eb205315c5affd18a95083d`  
		Last Modified: Thu, 15 Jan 2026 01:07:17 GMT  
		Size: 122.7 MB (122657613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3472e72d73ac3b924f65cb42f3e7414faf9e7496284fafb1c5bf78cbab6a735a`  
		Last Modified: Thu, 15 Jan 2026 01:06:59 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:fe3968e30977cde7c01f46ff921b1389c3c9a6803f06e0d85adb6917e14fd904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5565453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef5dc2cff512b217a0faa818e5f4d1fcdc5c05278b787cc97275508a120e2dc`

```dockerfile
```

-	Layers:
	-	`sha256:5e0bcc04be75b107f4391254e47c843ff5cc050fea95760db87e2e7983eefe26`  
		Last Modified: Thu, 15 Jan 2026 01:45:32 GMT  
		Size: 5.5 MB (5539693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50838335d46938630e13acec5047d86765db6491b2c740b55ebcef9a275bf0f7`  
		Last Modified: Thu, 15 Jan 2026 01:45:33 GMT  
		Size: 25.8 KB (25760 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6`

```console
$ docker pull ghost@sha256:86090f3ee57af8d8e3fa11875b5787068a1c17b8aebd4b88d932efe11097f578
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
$ docker pull ghost@sha256:ef3782910d75e1a4d0f2fee23d521f47ff4f2dd770a00d6cb4bd5a45c260165d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229949562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e67eca0fbe174babbedbd2b2dab2f54beefaf217dfe3b076edb2941c72d4181`
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
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:51 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:00 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:00 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:00 GMT
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
		Last Modified: Wed, 14 Jan 2026 17:59:37 GMT  
		Size: 49.5 MB (49472719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ac2b87b09265a60e104e3d87872d2c15f913cbbfd4d401b5e4b5353e4ced4`  
		Last Modified: Wed, 14 Jan 2026 17:59:48 GMT  
		Size: 1.7 MB (1712660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cc9ecead9d0fe8970f3923a484fcd4fe1fd027fab911d462ca552cd57d5dbf`  
		Last Modified: Wed, 14 Jan 2026 17:59:36 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d9069be84eda409daf000052287ded0488fa41932b208a91d7b5d9c61fb1db`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 1.2 MB (1247544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139dd34f662903c210b176797936f46c21e51067027a573dba8cf698eec3198`  
		Last Modified: Fri, 16 Jan 2026 21:53:42 GMT  
		Size: 11.7 MB (11704039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe03f721169025219aa078337a2541219c5ac7246fb867e8aff113d1e20b884`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 137.6 MB (137579701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54048a9e0fb4911913295adb6af4358c80b7065fbed3847c9f8896df95c8853`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:f0a051f5af0b039dad919753c3041d11088d11264a2d6b34202496fa65ceea68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5618877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aec6fe309a03ace913e95d0b5789af60ff41dc0a6518a6701233a74996e75f8`

```dockerfile
```

-	Layers:
	-	`sha256:939d78f65f1ccf8a812605765fcd939e938d2218ee6f2c787e8b9806c9a9c969`  
		Last Modified: Fri, 16 Jan 2026 22:45:38 GMT  
		Size: 5.6 MB (5592530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa662e79d45a5b6a60edcb33a6f22188c2cfa985ed1b67ef7d9bfef7ebb21087`  
		Last Modified: Fri, 16 Jan 2026 22:45:39 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm variant v7

```console
$ docker pull ghost@sha256:e710e94955768bd41a14f809d4d928e15a84d8a6245cc224dc99cf2ee2338d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221405328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ddf88f39a855f8364b0c92d1913a540fc11ec7b886d770172e17cab3fbf16a`
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
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:49:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:49:57 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:50:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:53:01 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:01 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:01 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:01 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
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
	-	`sha256:a249d6508920eeaed8c936fcd9d1266903a78701d8d719939629aecacd2b3612`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 1.2 MB (1214444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cecadaf268b53180de45b75d528261de3e54e528974811d9678e3ad073280`  
		Last Modified: Fri, 16 Jan 2026 21:53:48 GMT  
		Size: 11.7 MB (11694733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df3a8008132b7222b86b8fcf41e409341df064efb15cd0b2db76a2e43652440`  
		Last Modified: Fri, 16 Jan 2026 21:55:08 GMT  
		Size: 138.6 MB (138635032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a54b4827a3677d869daa769f728f3d85ed1c41810346c406ebdba1c9d6017bb`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:bbd9199cb4a5da33fb05a2c105163173092e1633d862b6c8b4709cf5dc9283e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5621812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b6b5679fb62f0751fd471ebda0daf079057a1d2440fb4f139bd37db503a5cb`

```dockerfile
```

-	Layers:
	-	`sha256:ecc780399baa396908b03e0e41b891f1866a69664c910d13f5c8f6839801370a`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 5.6 MB (5595327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b857b5e875c2615f4e29809571a4619dc21beb25493216bedf4002027ac0ab97`  
		Last Modified: Fri, 16 Jan 2026 22:45:45 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cd23414049a2774d17ae2dd1e327e1037e2ae277751e37e06a25cd0da6a35a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230013156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1383692cd7c356a7a82172e9a8f64527070c1550ab468edb794c3ecc7e285d09`
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
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:29 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:06 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:06 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:06 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87c15c864725a8daa5ca1505d5d886e53928b49fa578e7a35dc51a4be5b715d`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4c74fb4662b26fe96702c59c427e26bd0489a0a1c1c5960592b029426583e3`  
		Last Modified: Wed, 14 Jan 2026 18:01:50 GMT  
		Size: 49.6 MB (49611029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20454c8e368d7849b8d2669b17f01d47585f0d71a5b683c0c03997c8733f81d2`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 1.7 MB (1712623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6686bd0124e3e3612ac03ec0e58e60f1d86a689763f36ecade62f90a4f8d1ea`  
		Last Modified: Wed, 14 Jan 2026 18:01:49 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7033eb962607a955c6372a69ee5257aa923a8d39d76674bd162f2787d935f3a`  
		Last Modified: Fri, 16 Jan 2026 21:54:44 GMT  
		Size: 1.2 MB (1201530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7651bda82d46538be346d839ca10addf26d82eede645b669e55ce70b5f63385`  
		Last Modified: Fri, 16 Jan 2026 21:54:54 GMT  
		Size: 11.7 MB (11703412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc9b9f0753a93ea6ffa5029194830560b1d152496a86a2b86054592ebe5a0c3`  
		Last Modified: Fri, 16 Jan 2026 21:54:47 GMT  
		Size: 137.7 MB (137672344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd6c458dda55df446dcb602d8173c61779b73d3a0ccbf96b3ec524e423e9d3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:53 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:02e7bd8415afbd519cd16da0a7c5f58bed487547a747c2962e0a62f6fd97b13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5619410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834af9f6d47a9d1a26e9c3b13c3ff24c2bf447846c1f4deb20f4a369ccbaae4f`

```dockerfile
```

-	Layers:
	-	`sha256:0ddf820b5a6704d55ee73e6166e8dc592df42b3892756b31e43cd02d23d23cb8`  
		Last Modified: Fri, 16 Jan 2026 22:45:51 GMT  
		Size: 5.6 MB (5592881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05df5e3594cece8c76e3b739c4668dc514e605246c00962e575600b709e88a3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:43 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; s390x

```console
$ docker pull ghost@sha256:c3436627928b1b43d1456845ecbf82ba8d9e3a7e42f317f4a2a18b6a0f4dacfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231935344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43437d8327a686e5f5a504963fdc52b1d29e8051166b368362edf196278c856`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 21:22:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 21:23:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 21:23:44 GMT
CMD ["node"]
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 22:23:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 22:23:31 GMT
ENV NODE_ENV=production
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 15 Jan 2026 22:23:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:57:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:57:35 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:57:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:57:35 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:57:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d139ad9a3a58767f140c3201036e062e1a612d605a2d9ad8f971d9d78b53105`  
		Last Modified: Tue, 13 Jan 2026 02:16:16 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b8ffadc3140bf38490474eefe010b5d358986aad8d44529804b0743054faac`  
		Last Modified: Wed, 14 Jan 2026 21:24:32 GMT  
		Size: 49.7 MB (49677854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d962a7944bc35ac4232287b29129631cb30e0c2303fe9accd5060e13d10e417c`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 1.7 MB (1713059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b2eef94eee0b83f1a3d7a9599195e40b2dc80c3676e1214811bd87d43ba5c6`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9743a6eb0019afb918d9a783e9824fd189d217337fdd105c51b13324597390`  
		Last Modified: Thu, 15 Jan 2026 23:29:01 GMT  
		Size: 1.2 MB (1221797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dc1783fd9f5092bf435b4a7176f1ffa2e2a22e9cb73e36790448ef519cc84d`  
		Last Modified: Thu, 15 Jan 2026 22:27:23 GMT  
		Size: 11.7 MB (11713708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad56df80bd6319c74dfc884bd19c872678904e3b83a9172205691d51dccf11b`  
		Last Modified: Fri, 16 Jan 2026 21:58:54 GMT  
		Size: 140.7 MB (140720181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d310d3c0fa29617bb1c71502f8aa26ec106e911099b6ead0f3fe978b9fe79f3`  
		Last Modified: Fri, 16 Jan 2026 21:58:39 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:77c6a5256641362cf56117a966d9303ba1632d8372901ae78527d59d41ecb9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4c08dd2b8bd5bdf1989895beb8d39f88a2f595895b66edf7aad20ffbd6cf2e`

```dockerfile
```

-	Layers:
	-	`sha256:8bd1303d556029148a7040fb1ec53ec847e4cb6d399044f8f4b7e982cf607135`  
		Last Modified: Fri, 16 Jan 2026 21:58:30 GMT  
		Size: 5.6 MB (5586355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d098d8ceb9e37f70da4e29e97439abe0305c8aadae217d3666565b2e120f8e14`  
		Last Modified: Fri, 16 Jan 2026 22:45:59 GMT  
		Size: 26.3 KB (26346 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine`

```console
$ docker pull ghost@sha256:914e79639c3335775a3963897909c183751a4639c069f6a686b1f3ce634d87ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:17e5b1f5af110967679bf1396274c9f0230c12181a1b368028e30386c5523ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207580257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f321510e4d3eeefe9b778c2db896377c50f4fbd9b3d8839ad461f39258d4ec30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:58:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 17:58:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:58:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:59:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:59:03 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:50:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:04 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:57 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:52:58 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:52:58 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:52:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dda044491a389c13d0aa53e5cc14375121749b7401b4db1825fd97191528aa`  
		Last Modified: Wed, 14 Jan 2026 17:59:34 GMT  
		Size: 51.6 MB (51601845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5453a6a95efdb1bc3321878ea844e2c518f39aecd5f7f8a78e1b78d89a637e`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 1.3 MB (1262129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd007ec038c44249b9612b09663aa39b77c77bf71eeed265f47bf14154bce59c`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a042a68d544d0e6e4af4122ae40be7b77648d26905a2090b25bc7494bbb22840`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 821.9 KB (821904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153d1b71d487941b613e2eae005aabdf6f1626041fd953b1bad75dcd1bb5a5ec`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 928.3 KB (928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd27759c78d3456cb0a43fdcce8bc5257f49e71e5fac8bee7760338bf5947d1`  
		Last Modified: Fri, 16 Jan 2026 21:53:28 GMT  
		Size: 11.7 MB (11704085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f498c381e2c67fe0c5122d9a9e1c76d3b94b4a927da0a2d03229db33994733e`  
		Last Modified: Fri, 16 Jan 2026 21:53:31 GMT  
		Size: 137.4 MB (137400829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04924f1eec39098092b680ae31e7c72b272d50f5e6fb85e6f3ae274fc5c9068`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:a6c58b116386808827fae97b5cd4e4c369ccf8b0258ad7dd69e44d05cd6f4731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f2ec9918f583fccf6f21998f4f167e2a58ac920a836ac0505558d6b0390f0b`

```dockerfile
```

-	Layers:
	-	`sha256:13a8e432a2560ff262b164884933a7f97e6393fbfe9e855827e44dd85fbc4aa6`  
		Last Modified: Fri, 16 Jan 2026 22:45:47 GMT  
		Size: 3.4 MB (3380529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bcb20062eda86d699ac09b7c815241e18aad84beb68635a2f40175751eeb5f8`  
		Last Modified: Fri, 16 Jan 2026 22:45:48 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:56ca8e2e13d8384c602992ed334702c2ac15eb010d0d8dccd3b2f6a71a0067cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219446765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c2373454f0661e9b0ee88181e279d0134dc3bc9d86e612eecbecee29089148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:28:46 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 18:28:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:46 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:28:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:28:49 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:51:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:37 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:29 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:29 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:29 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88a575fc12781c98ff7a5b3d03ea1b36814176fddaf1e55e0b1bb14bc6c34e4`  
		Last Modified: Wed, 14 Jan 2026 18:29:25 GMT  
		Size: 52.2 MB (52237556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8623286f7776425bdee32d428d0c53f4acc0d836ec7ac19fff597b59095a9e`  
		Last Modified: Wed, 14 Jan 2026 18:29:14 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed93f8843f88facc599516714a1f82921aa4778c5fec480d0e4ab5410c54695`  
		Last Modified: Wed, 14 Jan 2026 18:29:04 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306c771ee35c6cec4a540617727df3f40b9a5c232a5a4094a4bf72dbbd4f4f61`  
		Last Modified: Fri, 16 Jan 2026 21:55:18 GMT  
		Size: 891.3 KB (891301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9733ede21bc1c0310cf194d38777508c5427c1e9f9fd6d6443208b1c07ad3a8c`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 881.3 KB (881291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a638dd4f153662af93a01c15f7b866acc2fa88d5160b92b317699d9ff56ef2ce`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 11.7 MB (11703289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dab10d9a81f61bdd780ff327a8d1d829b8b2f4babeb70aa93cc854881b1c91a`  
		Last Modified: Fri, 16 Jan 2026 21:55:10 GMT  
		Size: 148.3 MB (148273578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a7bc6e0a1ffaf5fb2be6585bba15cd3bcf026dc6794580f0b5b03a090125d4`  
		Last Modified: Fri, 16 Jan 2026 21:55:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:be3ff6e8c6c43594c2e6f87aa27c1afe2a96a01d0537ee1200f269baf1e72814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29859ce48bfbb7b6978182944457e7c0209806800411d1da893a96a7a06ee01`

```dockerfile
```

-	Layers:
	-	`sha256:5f9331badabe199f703be07f013eea0245f7b3da4bc86518f347d46dd0a52707`  
		Last Modified: Fri, 16 Jan 2026 22:45:53 GMT  
		Size: 3.4 MB (3380035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c33f5ddc0479111797b425a08e20e85f80919522a33eba654bb5d229b194b2`  
		Last Modified: Fri, 16 Jan 2026 22:45:54 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine3.23`

```console
$ docker pull ghost@sha256:914e79639c3335775a3963897909c183751a4639c069f6a686b1f3ce634d87ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:17e5b1f5af110967679bf1396274c9f0230c12181a1b368028e30386c5523ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207580257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f321510e4d3eeefe9b778c2db896377c50f4fbd9b3d8839ad461f39258d4ec30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:58:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 17:58:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:58:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:59:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:59:03 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:50:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:04 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:57 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:52:58 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:52:58 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:52:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dda044491a389c13d0aa53e5cc14375121749b7401b4db1825fd97191528aa`  
		Last Modified: Wed, 14 Jan 2026 17:59:34 GMT  
		Size: 51.6 MB (51601845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5453a6a95efdb1bc3321878ea844e2c518f39aecd5f7f8a78e1b78d89a637e`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 1.3 MB (1262129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd007ec038c44249b9612b09663aa39b77c77bf71eeed265f47bf14154bce59c`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a042a68d544d0e6e4af4122ae40be7b77648d26905a2090b25bc7494bbb22840`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 821.9 KB (821904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153d1b71d487941b613e2eae005aabdf6f1626041fd953b1bad75dcd1bb5a5ec`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 928.3 KB (928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd27759c78d3456cb0a43fdcce8bc5257f49e71e5fac8bee7760338bf5947d1`  
		Last Modified: Fri, 16 Jan 2026 21:53:28 GMT  
		Size: 11.7 MB (11704085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f498c381e2c67fe0c5122d9a9e1c76d3b94b4a927da0a2d03229db33994733e`  
		Last Modified: Fri, 16 Jan 2026 21:53:31 GMT  
		Size: 137.4 MB (137400829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04924f1eec39098092b680ae31e7c72b272d50f5e6fb85e6f3ae274fc5c9068`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:a6c58b116386808827fae97b5cd4e4c369ccf8b0258ad7dd69e44d05cd6f4731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f2ec9918f583fccf6f21998f4f167e2a58ac920a836ac0505558d6b0390f0b`

```dockerfile
```

-	Layers:
	-	`sha256:13a8e432a2560ff262b164884933a7f97e6393fbfe9e855827e44dd85fbc4aa6`  
		Last Modified: Fri, 16 Jan 2026 22:45:47 GMT  
		Size: 3.4 MB (3380529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bcb20062eda86d699ac09b7c815241e18aad84beb68635a2f40175751eeb5f8`  
		Last Modified: Fri, 16 Jan 2026 22:45:48 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:56ca8e2e13d8384c602992ed334702c2ac15eb010d0d8dccd3b2f6a71a0067cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219446765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c2373454f0661e9b0ee88181e279d0134dc3bc9d86e612eecbecee29089148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:28:46 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 18:28:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:46 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:28:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:28:49 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:51:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:37 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:29 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:29 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:29 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88a575fc12781c98ff7a5b3d03ea1b36814176fddaf1e55e0b1bb14bc6c34e4`  
		Last Modified: Wed, 14 Jan 2026 18:29:25 GMT  
		Size: 52.2 MB (52237556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8623286f7776425bdee32d428d0c53f4acc0d836ec7ac19fff597b59095a9e`  
		Last Modified: Wed, 14 Jan 2026 18:29:14 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed93f8843f88facc599516714a1f82921aa4778c5fec480d0e4ab5410c54695`  
		Last Modified: Wed, 14 Jan 2026 18:29:04 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306c771ee35c6cec4a540617727df3f40b9a5c232a5a4094a4bf72dbbd4f4f61`  
		Last Modified: Fri, 16 Jan 2026 21:55:18 GMT  
		Size: 891.3 KB (891301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9733ede21bc1c0310cf194d38777508c5427c1e9f9fd6d6443208b1c07ad3a8c`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 881.3 KB (881291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a638dd4f153662af93a01c15f7b866acc2fa88d5160b92b317699d9ff56ef2ce`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 11.7 MB (11703289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dab10d9a81f61bdd780ff327a8d1d829b8b2f4babeb70aa93cc854881b1c91a`  
		Last Modified: Fri, 16 Jan 2026 21:55:10 GMT  
		Size: 148.3 MB (148273578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a7bc6e0a1ffaf5fb2be6585bba15cd3bcf026dc6794580f0b5b03a090125d4`  
		Last Modified: Fri, 16 Jan 2026 21:55:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:be3ff6e8c6c43594c2e6f87aa27c1afe2a96a01d0537ee1200f269baf1e72814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29859ce48bfbb7b6978182944457e7c0209806800411d1da893a96a7a06ee01`

```dockerfile
```

-	Layers:
	-	`sha256:5f9331badabe199f703be07f013eea0245f7b3da4bc86518f347d46dd0a52707`  
		Last Modified: Fri, 16 Jan 2026 22:45:53 GMT  
		Size: 3.4 MB (3380035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c33f5ddc0479111797b425a08e20e85f80919522a33eba654bb5d229b194b2`  
		Last Modified: Fri, 16 Jan 2026 22:45:54 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-bookworm`

```console
$ docker pull ghost@sha256:86090f3ee57af8d8e3fa11875b5787068a1c17b8aebd4b88d932efe11097f578
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
$ docker pull ghost@sha256:ef3782910d75e1a4d0f2fee23d521f47ff4f2dd770a00d6cb4bd5a45c260165d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229949562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e67eca0fbe174babbedbd2b2dab2f54beefaf217dfe3b076edb2941c72d4181`
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
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:51 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:00 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:00 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:00 GMT
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
		Last Modified: Wed, 14 Jan 2026 17:59:37 GMT  
		Size: 49.5 MB (49472719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ac2b87b09265a60e104e3d87872d2c15f913cbbfd4d401b5e4b5353e4ced4`  
		Last Modified: Wed, 14 Jan 2026 17:59:48 GMT  
		Size: 1.7 MB (1712660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cc9ecead9d0fe8970f3923a484fcd4fe1fd027fab911d462ca552cd57d5dbf`  
		Last Modified: Wed, 14 Jan 2026 17:59:36 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d9069be84eda409daf000052287ded0488fa41932b208a91d7b5d9c61fb1db`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 1.2 MB (1247544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139dd34f662903c210b176797936f46c21e51067027a573dba8cf698eec3198`  
		Last Modified: Fri, 16 Jan 2026 21:53:42 GMT  
		Size: 11.7 MB (11704039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe03f721169025219aa078337a2541219c5ac7246fb867e8aff113d1e20b884`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 137.6 MB (137579701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54048a9e0fb4911913295adb6af4358c80b7065fbed3847c9f8896df95c8853`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:f0a051f5af0b039dad919753c3041d11088d11264a2d6b34202496fa65ceea68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5618877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aec6fe309a03ace913e95d0b5789af60ff41dc0a6518a6701233a74996e75f8`

```dockerfile
```

-	Layers:
	-	`sha256:939d78f65f1ccf8a812605765fcd939e938d2218ee6f2c787e8b9806c9a9c969`  
		Last Modified: Fri, 16 Jan 2026 22:45:38 GMT  
		Size: 5.6 MB (5592530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa662e79d45a5b6a60edcb33a6f22188c2cfa985ed1b67ef7d9bfef7ebb21087`  
		Last Modified: Fri, 16 Jan 2026 22:45:39 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:e710e94955768bd41a14f809d4d928e15a84d8a6245cc224dc99cf2ee2338d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221405328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ddf88f39a855f8364b0c92d1913a540fc11ec7b886d770172e17cab3fbf16a`
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
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:49:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:49:57 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:50:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:53:01 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:01 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:01 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:01 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
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
	-	`sha256:a249d6508920eeaed8c936fcd9d1266903a78701d8d719939629aecacd2b3612`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 1.2 MB (1214444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cecadaf268b53180de45b75d528261de3e54e528974811d9678e3ad073280`  
		Last Modified: Fri, 16 Jan 2026 21:53:48 GMT  
		Size: 11.7 MB (11694733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df3a8008132b7222b86b8fcf41e409341df064efb15cd0b2db76a2e43652440`  
		Last Modified: Fri, 16 Jan 2026 21:55:08 GMT  
		Size: 138.6 MB (138635032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a54b4827a3677d869daa769f728f3d85ed1c41810346c406ebdba1c9d6017bb`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:bbd9199cb4a5da33fb05a2c105163173092e1633d862b6c8b4709cf5dc9283e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5621812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b6b5679fb62f0751fd471ebda0daf079057a1d2440fb4f139bd37db503a5cb`

```dockerfile
```

-	Layers:
	-	`sha256:ecc780399baa396908b03e0e41b891f1866a69664c910d13f5c8f6839801370a`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 5.6 MB (5595327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b857b5e875c2615f4e29809571a4619dc21beb25493216bedf4002027ac0ab97`  
		Last Modified: Fri, 16 Jan 2026 22:45:45 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cd23414049a2774d17ae2dd1e327e1037e2ae277751e37e06a25cd0da6a35a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230013156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1383692cd7c356a7a82172e9a8f64527070c1550ab468edb794c3ecc7e285d09`
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
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:29 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:06 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:06 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:06 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87c15c864725a8daa5ca1505d5d886e53928b49fa578e7a35dc51a4be5b715d`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4c74fb4662b26fe96702c59c427e26bd0489a0a1c1c5960592b029426583e3`  
		Last Modified: Wed, 14 Jan 2026 18:01:50 GMT  
		Size: 49.6 MB (49611029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20454c8e368d7849b8d2669b17f01d47585f0d71a5b683c0c03997c8733f81d2`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 1.7 MB (1712623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6686bd0124e3e3612ac03ec0e58e60f1d86a689763f36ecade62f90a4f8d1ea`  
		Last Modified: Wed, 14 Jan 2026 18:01:49 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7033eb962607a955c6372a69ee5257aa923a8d39d76674bd162f2787d935f3a`  
		Last Modified: Fri, 16 Jan 2026 21:54:44 GMT  
		Size: 1.2 MB (1201530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7651bda82d46538be346d839ca10addf26d82eede645b669e55ce70b5f63385`  
		Last Modified: Fri, 16 Jan 2026 21:54:54 GMT  
		Size: 11.7 MB (11703412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc9b9f0753a93ea6ffa5029194830560b1d152496a86a2b86054592ebe5a0c3`  
		Last Modified: Fri, 16 Jan 2026 21:54:47 GMT  
		Size: 137.7 MB (137672344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd6c458dda55df446dcb602d8173c61779b73d3a0ccbf96b3ec524e423e9d3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:53 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:02e7bd8415afbd519cd16da0a7c5f58bed487547a747c2962e0a62f6fd97b13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5619410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834af9f6d47a9d1a26e9c3b13c3ff24c2bf447846c1f4deb20f4a369ccbaae4f`

```dockerfile
```

-	Layers:
	-	`sha256:0ddf820b5a6704d55ee73e6166e8dc592df42b3892756b31e43cd02d23d23cb8`  
		Last Modified: Fri, 16 Jan 2026 22:45:51 GMT  
		Size: 5.6 MB (5592881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05df5e3594cece8c76e3b739c4668dc514e605246c00962e575600b709e88a3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:43 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:c3436627928b1b43d1456845ecbf82ba8d9e3a7e42f317f4a2a18b6a0f4dacfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231935344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43437d8327a686e5f5a504963fdc52b1d29e8051166b368362edf196278c856`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 21:22:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 21:23:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 21:23:44 GMT
CMD ["node"]
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 22:23:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 22:23:31 GMT
ENV NODE_ENV=production
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 15 Jan 2026 22:23:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:57:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:57:35 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:57:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:57:35 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:57:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d139ad9a3a58767f140c3201036e062e1a612d605a2d9ad8f971d9d78b53105`  
		Last Modified: Tue, 13 Jan 2026 02:16:16 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b8ffadc3140bf38490474eefe010b5d358986aad8d44529804b0743054faac`  
		Last Modified: Wed, 14 Jan 2026 21:24:32 GMT  
		Size: 49.7 MB (49677854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d962a7944bc35ac4232287b29129631cb30e0c2303fe9accd5060e13d10e417c`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 1.7 MB (1713059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b2eef94eee0b83f1a3d7a9599195e40b2dc80c3676e1214811bd87d43ba5c6`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9743a6eb0019afb918d9a783e9824fd189d217337fdd105c51b13324597390`  
		Last Modified: Thu, 15 Jan 2026 23:29:01 GMT  
		Size: 1.2 MB (1221797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dc1783fd9f5092bf435b4a7176f1ffa2e2a22e9cb73e36790448ef519cc84d`  
		Last Modified: Thu, 15 Jan 2026 22:27:23 GMT  
		Size: 11.7 MB (11713708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad56df80bd6319c74dfc884bd19c872678904e3b83a9172205691d51dccf11b`  
		Last Modified: Fri, 16 Jan 2026 21:58:54 GMT  
		Size: 140.7 MB (140720181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d310d3c0fa29617bb1c71502f8aa26ec106e911099b6ead0f3fe978b9fe79f3`  
		Last Modified: Fri, 16 Jan 2026 21:58:39 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:77c6a5256641362cf56117a966d9303ba1632d8372901ae78527d59d41ecb9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4c08dd2b8bd5bdf1989895beb8d39f88a2f595895b66edf7aad20ffbd6cf2e`

```dockerfile
```

-	Layers:
	-	`sha256:8bd1303d556029148a7040fb1ec53ec847e4cb6d399044f8f4b7e982cf607135`  
		Last Modified: Fri, 16 Jan 2026 21:58:30 GMT  
		Size: 5.6 MB (5586355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d098d8ceb9e37f70da4e29e97439abe0305c8aadae217d3666565b2e120f8e14`  
		Last Modified: Fri, 16 Jan 2026 22:45:59 GMT  
		Size: 26.3 KB (26346 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.13`

```console
$ docker pull ghost@sha256:86090f3ee57af8d8e3fa11875b5787068a1c17b8aebd4b88d932efe11097f578
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

### `ghost:6.13` - linux; amd64

```console
$ docker pull ghost@sha256:ef3782910d75e1a4d0f2fee23d521f47ff4f2dd770a00d6cb4bd5a45c260165d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229949562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e67eca0fbe174babbedbd2b2dab2f54beefaf217dfe3b076edb2941c72d4181`
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
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:51 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:00 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:00 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:00 GMT
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
		Last Modified: Wed, 14 Jan 2026 17:59:37 GMT  
		Size: 49.5 MB (49472719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ac2b87b09265a60e104e3d87872d2c15f913cbbfd4d401b5e4b5353e4ced4`  
		Last Modified: Wed, 14 Jan 2026 17:59:48 GMT  
		Size: 1.7 MB (1712660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cc9ecead9d0fe8970f3923a484fcd4fe1fd027fab911d462ca552cd57d5dbf`  
		Last Modified: Wed, 14 Jan 2026 17:59:36 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d9069be84eda409daf000052287ded0488fa41932b208a91d7b5d9c61fb1db`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 1.2 MB (1247544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139dd34f662903c210b176797936f46c21e51067027a573dba8cf698eec3198`  
		Last Modified: Fri, 16 Jan 2026 21:53:42 GMT  
		Size: 11.7 MB (11704039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe03f721169025219aa078337a2541219c5ac7246fb867e8aff113d1e20b884`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 137.6 MB (137579701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54048a9e0fb4911913295adb6af4358c80b7065fbed3847c9f8896df95c8853`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13` - unknown; unknown

```console
$ docker pull ghost@sha256:f0a051f5af0b039dad919753c3041d11088d11264a2d6b34202496fa65ceea68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5618877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aec6fe309a03ace913e95d0b5789af60ff41dc0a6518a6701233a74996e75f8`

```dockerfile
```

-	Layers:
	-	`sha256:939d78f65f1ccf8a812605765fcd939e938d2218ee6f2c787e8b9806c9a9c969`  
		Last Modified: Fri, 16 Jan 2026 22:45:38 GMT  
		Size: 5.6 MB (5592530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa662e79d45a5b6a60edcb33a6f22188c2cfa985ed1b67ef7d9bfef7ebb21087`  
		Last Modified: Fri, 16 Jan 2026 22:45:39 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13` - linux; arm variant v7

```console
$ docker pull ghost@sha256:e710e94955768bd41a14f809d4d928e15a84d8a6245cc224dc99cf2ee2338d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221405328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ddf88f39a855f8364b0c92d1913a540fc11ec7b886d770172e17cab3fbf16a`
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
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:49:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:49:57 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:50:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:53:01 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:01 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:01 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:01 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
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
	-	`sha256:a249d6508920eeaed8c936fcd9d1266903a78701d8d719939629aecacd2b3612`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 1.2 MB (1214444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cecadaf268b53180de45b75d528261de3e54e528974811d9678e3ad073280`  
		Last Modified: Fri, 16 Jan 2026 21:53:48 GMT  
		Size: 11.7 MB (11694733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df3a8008132b7222b86b8fcf41e409341df064efb15cd0b2db76a2e43652440`  
		Last Modified: Fri, 16 Jan 2026 21:55:08 GMT  
		Size: 138.6 MB (138635032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a54b4827a3677d869daa769f728f3d85ed1c41810346c406ebdba1c9d6017bb`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13` - unknown; unknown

```console
$ docker pull ghost@sha256:bbd9199cb4a5da33fb05a2c105163173092e1633d862b6c8b4709cf5dc9283e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5621812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b6b5679fb62f0751fd471ebda0daf079057a1d2440fb4f139bd37db503a5cb`

```dockerfile
```

-	Layers:
	-	`sha256:ecc780399baa396908b03e0e41b891f1866a69664c910d13f5c8f6839801370a`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 5.6 MB (5595327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b857b5e875c2615f4e29809571a4619dc21beb25493216bedf4002027ac0ab97`  
		Last Modified: Fri, 16 Jan 2026 22:45:45 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cd23414049a2774d17ae2dd1e327e1037e2ae277751e37e06a25cd0da6a35a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230013156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1383692cd7c356a7a82172e9a8f64527070c1550ab468edb794c3ecc7e285d09`
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
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:29 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:06 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:06 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:06 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87c15c864725a8daa5ca1505d5d886e53928b49fa578e7a35dc51a4be5b715d`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4c74fb4662b26fe96702c59c427e26bd0489a0a1c1c5960592b029426583e3`  
		Last Modified: Wed, 14 Jan 2026 18:01:50 GMT  
		Size: 49.6 MB (49611029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20454c8e368d7849b8d2669b17f01d47585f0d71a5b683c0c03997c8733f81d2`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 1.7 MB (1712623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6686bd0124e3e3612ac03ec0e58e60f1d86a689763f36ecade62f90a4f8d1ea`  
		Last Modified: Wed, 14 Jan 2026 18:01:49 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7033eb962607a955c6372a69ee5257aa923a8d39d76674bd162f2787d935f3a`  
		Last Modified: Fri, 16 Jan 2026 21:54:44 GMT  
		Size: 1.2 MB (1201530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7651bda82d46538be346d839ca10addf26d82eede645b669e55ce70b5f63385`  
		Last Modified: Fri, 16 Jan 2026 21:54:54 GMT  
		Size: 11.7 MB (11703412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc9b9f0753a93ea6ffa5029194830560b1d152496a86a2b86054592ebe5a0c3`  
		Last Modified: Fri, 16 Jan 2026 21:54:47 GMT  
		Size: 137.7 MB (137672344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd6c458dda55df446dcb602d8173c61779b73d3a0ccbf96b3ec524e423e9d3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:53 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13` - unknown; unknown

```console
$ docker pull ghost@sha256:02e7bd8415afbd519cd16da0a7c5f58bed487547a747c2962e0a62f6fd97b13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5619410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834af9f6d47a9d1a26e9c3b13c3ff24c2bf447846c1f4deb20f4a369ccbaae4f`

```dockerfile
```

-	Layers:
	-	`sha256:0ddf820b5a6704d55ee73e6166e8dc592df42b3892756b31e43cd02d23d23cb8`  
		Last Modified: Fri, 16 Jan 2026 22:45:51 GMT  
		Size: 5.6 MB (5592881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05df5e3594cece8c76e3b739c4668dc514e605246c00962e575600b709e88a3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:43 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13` - linux; s390x

```console
$ docker pull ghost@sha256:c3436627928b1b43d1456845ecbf82ba8d9e3a7e42f317f4a2a18b6a0f4dacfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231935344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43437d8327a686e5f5a504963fdc52b1d29e8051166b368362edf196278c856`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 21:22:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 21:23:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 21:23:44 GMT
CMD ["node"]
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 22:23:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 22:23:31 GMT
ENV NODE_ENV=production
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 15 Jan 2026 22:23:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:57:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:57:35 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:57:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:57:35 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:57:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d139ad9a3a58767f140c3201036e062e1a612d605a2d9ad8f971d9d78b53105`  
		Last Modified: Tue, 13 Jan 2026 02:16:16 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b8ffadc3140bf38490474eefe010b5d358986aad8d44529804b0743054faac`  
		Last Modified: Wed, 14 Jan 2026 21:24:32 GMT  
		Size: 49.7 MB (49677854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d962a7944bc35ac4232287b29129631cb30e0c2303fe9accd5060e13d10e417c`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 1.7 MB (1713059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b2eef94eee0b83f1a3d7a9599195e40b2dc80c3676e1214811bd87d43ba5c6`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9743a6eb0019afb918d9a783e9824fd189d217337fdd105c51b13324597390`  
		Last Modified: Thu, 15 Jan 2026 23:29:01 GMT  
		Size: 1.2 MB (1221797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dc1783fd9f5092bf435b4a7176f1ffa2e2a22e9cb73e36790448ef519cc84d`  
		Last Modified: Thu, 15 Jan 2026 22:27:23 GMT  
		Size: 11.7 MB (11713708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad56df80bd6319c74dfc884bd19c872678904e3b83a9172205691d51dccf11b`  
		Last Modified: Fri, 16 Jan 2026 21:58:54 GMT  
		Size: 140.7 MB (140720181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d310d3c0fa29617bb1c71502f8aa26ec106e911099b6ead0f3fe978b9fe79f3`  
		Last Modified: Fri, 16 Jan 2026 21:58:39 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13` - unknown; unknown

```console
$ docker pull ghost@sha256:77c6a5256641362cf56117a966d9303ba1632d8372901ae78527d59d41ecb9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4c08dd2b8bd5bdf1989895beb8d39f88a2f595895b66edf7aad20ffbd6cf2e`

```dockerfile
```

-	Layers:
	-	`sha256:8bd1303d556029148a7040fb1ec53ec847e4cb6d399044f8f4b7e982cf607135`  
		Last Modified: Fri, 16 Jan 2026 21:58:30 GMT  
		Size: 5.6 MB (5586355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d098d8ceb9e37f70da4e29e97439abe0305c8aadae217d3666565b2e120f8e14`  
		Last Modified: Fri, 16 Jan 2026 22:45:59 GMT  
		Size: 26.3 KB (26346 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.13-alpine`

```console
$ docker pull ghost@sha256:914e79639c3335775a3963897909c183751a4639c069f6a686b1f3ce634d87ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.13-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:17e5b1f5af110967679bf1396274c9f0230c12181a1b368028e30386c5523ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207580257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f321510e4d3eeefe9b778c2db896377c50f4fbd9b3d8839ad461f39258d4ec30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:58:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 17:58:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:58:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:59:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:59:03 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:50:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:04 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:57 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:52:58 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:52:58 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:52:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dda044491a389c13d0aa53e5cc14375121749b7401b4db1825fd97191528aa`  
		Last Modified: Wed, 14 Jan 2026 17:59:34 GMT  
		Size: 51.6 MB (51601845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5453a6a95efdb1bc3321878ea844e2c518f39aecd5f7f8a78e1b78d89a637e`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 1.3 MB (1262129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd007ec038c44249b9612b09663aa39b77c77bf71eeed265f47bf14154bce59c`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a042a68d544d0e6e4af4122ae40be7b77648d26905a2090b25bc7494bbb22840`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 821.9 KB (821904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153d1b71d487941b613e2eae005aabdf6f1626041fd953b1bad75dcd1bb5a5ec`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 928.3 KB (928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd27759c78d3456cb0a43fdcce8bc5257f49e71e5fac8bee7760338bf5947d1`  
		Last Modified: Fri, 16 Jan 2026 21:53:28 GMT  
		Size: 11.7 MB (11704085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f498c381e2c67fe0c5122d9a9e1c76d3b94b4a927da0a2d03229db33994733e`  
		Last Modified: Fri, 16 Jan 2026 21:53:31 GMT  
		Size: 137.4 MB (137400829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04924f1eec39098092b680ae31e7c72b272d50f5e6fb85e6f3ae274fc5c9068`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:a6c58b116386808827fae97b5cd4e4c369ccf8b0258ad7dd69e44d05cd6f4731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f2ec9918f583fccf6f21998f4f167e2a58ac920a836ac0505558d6b0390f0b`

```dockerfile
```

-	Layers:
	-	`sha256:13a8e432a2560ff262b164884933a7f97e6393fbfe9e855827e44dd85fbc4aa6`  
		Last Modified: Fri, 16 Jan 2026 22:45:47 GMT  
		Size: 3.4 MB (3380529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bcb20062eda86d699ac09b7c815241e18aad84beb68635a2f40175751eeb5f8`  
		Last Modified: Fri, 16 Jan 2026 22:45:48 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:56ca8e2e13d8384c602992ed334702c2ac15eb010d0d8dccd3b2f6a71a0067cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219446765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c2373454f0661e9b0ee88181e279d0134dc3bc9d86e612eecbecee29089148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:28:46 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 18:28:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:46 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:28:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:28:49 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:51:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:37 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:29 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:29 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:29 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88a575fc12781c98ff7a5b3d03ea1b36814176fddaf1e55e0b1bb14bc6c34e4`  
		Last Modified: Wed, 14 Jan 2026 18:29:25 GMT  
		Size: 52.2 MB (52237556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8623286f7776425bdee32d428d0c53f4acc0d836ec7ac19fff597b59095a9e`  
		Last Modified: Wed, 14 Jan 2026 18:29:14 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed93f8843f88facc599516714a1f82921aa4778c5fec480d0e4ab5410c54695`  
		Last Modified: Wed, 14 Jan 2026 18:29:04 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306c771ee35c6cec4a540617727df3f40b9a5c232a5a4094a4bf72dbbd4f4f61`  
		Last Modified: Fri, 16 Jan 2026 21:55:18 GMT  
		Size: 891.3 KB (891301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9733ede21bc1c0310cf194d38777508c5427c1e9f9fd6d6443208b1c07ad3a8c`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 881.3 KB (881291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a638dd4f153662af93a01c15f7b866acc2fa88d5160b92b317699d9ff56ef2ce`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 11.7 MB (11703289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dab10d9a81f61bdd780ff327a8d1d829b8b2f4babeb70aa93cc854881b1c91a`  
		Last Modified: Fri, 16 Jan 2026 21:55:10 GMT  
		Size: 148.3 MB (148273578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a7bc6e0a1ffaf5fb2be6585bba15cd3bcf026dc6794580f0b5b03a090125d4`  
		Last Modified: Fri, 16 Jan 2026 21:55:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:be3ff6e8c6c43594c2e6f87aa27c1afe2a96a01d0537ee1200f269baf1e72814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29859ce48bfbb7b6978182944457e7c0209806800411d1da893a96a7a06ee01`

```dockerfile
```

-	Layers:
	-	`sha256:5f9331badabe199f703be07f013eea0245f7b3da4bc86518f347d46dd0a52707`  
		Last Modified: Fri, 16 Jan 2026 22:45:53 GMT  
		Size: 3.4 MB (3380035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c33f5ddc0479111797b425a08e20e85f80919522a33eba654bb5d229b194b2`  
		Last Modified: Fri, 16 Jan 2026 22:45:54 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.13-alpine3.23`

```console
$ docker pull ghost@sha256:914e79639c3335775a3963897909c183751a4639c069f6a686b1f3ce634d87ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.13-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:17e5b1f5af110967679bf1396274c9f0230c12181a1b368028e30386c5523ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207580257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f321510e4d3eeefe9b778c2db896377c50f4fbd9b3d8839ad461f39258d4ec30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:58:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 17:58:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:58:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:59:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:59:03 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:50:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:04 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:57 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:52:58 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:52:58 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:52:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dda044491a389c13d0aa53e5cc14375121749b7401b4db1825fd97191528aa`  
		Last Modified: Wed, 14 Jan 2026 17:59:34 GMT  
		Size: 51.6 MB (51601845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5453a6a95efdb1bc3321878ea844e2c518f39aecd5f7f8a78e1b78d89a637e`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 1.3 MB (1262129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd007ec038c44249b9612b09663aa39b77c77bf71eeed265f47bf14154bce59c`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a042a68d544d0e6e4af4122ae40be7b77648d26905a2090b25bc7494bbb22840`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 821.9 KB (821904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153d1b71d487941b613e2eae005aabdf6f1626041fd953b1bad75dcd1bb5a5ec`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 928.3 KB (928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd27759c78d3456cb0a43fdcce8bc5257f49e71e5fac8bee7760338bf5947d1`  
		Last Modified: Fri, 16 Jan 2026 21:53:28 GMT  
		Size: 11.7 MB (11704085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f498c381e2c67fe0c5122d9a9e1c76d3b94b4a927da0a2d03229db33994733e`  
		Last Modified: Fri, 16 Jan 2026 21:53:31 GMT  
		Size: 137.4 MB (137400829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04924f1eec39098092b680ae31e7c72b272d50f5e6fb85e6f3ae274fc5c9068`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:a6c58b116386808827fae97b5cd4e4c369ccf8b0258ad7dd69e44d05cd6f4731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f2ec9918f583fccf6f21998f4f167e2a58ac920a836ac0505558d6b0390f0b`

```dockerfile
```

-	Layers:
	-	`sha256:13a8e432a2560ff262b164884933a7f97e6393fbfe9e855827e44dd85fbc4aa6`  
		Last Modified: Fri, 16 Jan 2026 22:45:47 GMT  
		Size: 3.4 MB (3380529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bcb20062eda86d699ac09b7c815241e18aad84beb68635a2f40175751eeb5f8`  
		Last Modified: Fri, 16 Jan 2026 22:45:48 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:56ca8e2e13d8384c602992ed334702c2ac15eb010d0d8dccd3b2f6a71a0067cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219446765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c2373454f0661e9b0ee88181e279d0134dc3bc9d86e612eecbecee29089148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:28:46 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 18:28:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:46 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:28:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:28:49 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:51:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:37 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:29 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:29 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:29 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88a575fc12781c98ff7a5b3d03ea1b36814176fddaf1e55e0b1bb14bc6c34e4`  
		Last Modified: Wed, 14 Jan 2026 18:29:25 GMT  
		Size: 52.2 MB (52237556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8623286f7776425bdee32d428d0c53f4acc0d836ec7ac19fff597b59095a9e`  
		Last Modified: Wed, 14 Jan 2026 18:29:14 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed93f8843f88facc599516714a1f82921aa4778c5fec480d0e4ab5410c54695`  
		Last Modified: Wed, 14 Jan 2026 18:29:04 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306c771ee35c6cec4a540617727df3f40b9a5c232a5a4094a4bf72dbbd4f4f61`  
		Last Modified: Fri, 16 Jan 2026 21:55:18 GMT  
		Size: 891.3 KB (891301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9733ede21bc1c0310cf194d38777508c5427c1e9f9fd6d6443208b1c07ad3a8c`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 881.3 KB (881291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a638dd4f153662af93a01c15f7b866acc2fa88d5160b92b317699d9ff56ef2ce`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 11.7 MB (11703289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dab10d9a81f61bdd780ff327a8d1d829b8b2f4babeb70aa93cc854881b1c91a`  
		Last Modified: Fri, 16 Jan 2026 21:55:10 GMT  
		Size: 148.3 MB (148273578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a7bc6e0a1ffaf5fb2be6585bba15cd3bcf026dc6794580f0b5b03a090125d4`  
		Last Modified: Fri, 16 Jan 2026 21:55:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:be3ff6e8c6c43594c2e6f87aa27c1afe2a96a01d0537ee1200f269baf1e72814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29859ce48bfbb7b6978182944457e7c0209806800411d1da893a96a7a06ee01`

```dockerfile
```

-	Layers:
	-	`sha256:5f9331badabe199f703be07f013eea0245f7b3da4bc86518f347d46dd0a52707`  
		Last Modified: Fri, 16 Jan 2026 22:45:53 GMT  
		Size: 3.4 MB (3380035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c33f5ddc0479111797b425a08e20e85f80919522a33eba654bb5d229b194b2`  
		Last Modified: Fri, 16 Jan 2026 22:45:54 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.13-bookworm`

```console
$ docker pull ghost@sha256:86090f3ee57af8d8e3fa11875b5787068a1c17b8aebd4b88d932efe11097f578
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

### `ghost:6.13-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:ef3782910d75e1a4d0f2fee23d521f47ff4f2dd770a00d6cb4bd5a45c260165d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229949562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e67eca0fbe174babbedbd2b2dab2f54beefaf217dfe3b076edb2941c72d4181`
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
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:51 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:00 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:00 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:00 GMT
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
		Last Modified: Wed, 14 Jan 2026 17:59:37 GMT  
		Size: 49.5 MB (49472719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ac2b87b09265a60e104e3d87872d2c15f913cbbfd4d401b5e4b5353e4ced4`  
		Last Modified: Wed, 14 Jan 2026 17:59:48 GMT  
		Size: 1.7 MB (1712660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cc9ecead9d0fe8970f3923a484fcd4fe1fd027fab911d462ca552cd57d5dbf`  
		Last Modified: Wed, 14 Jan 2026 17:59:36 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d9069be84eda409daf000052287ded0488fa41932b208a91d7b5d9c61fb1db`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 1.2 MB (1247544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139dd34f662903c210b176797936f46c21e51067027a573dba8cf698eec3198`  
		Last Modified: Fri, 16 Jan 2026 21:53:42 GMT  
		Size: 11.7 MB (11704039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe03f721169025219aa078337a2541219c5ac7246fb867e8aff113d1e20b884`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 137.6 MB (137579701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54048a9e0fb4911913295adb6af4358c80b7065fbed3847c9f8896df95c8853`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:f0a051f5af0b039dad919753c3041d11088d11264a2d6b34202496fa65ceea68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5618877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aec6fe309a03ace913e95d0b5789af60ff41dc0a6518a6701233a74996e75f8`

```dockerfile
```

-	Layers:
	-	`sha256:939d78f65f1ccf8a812605765fcd939e938d2218ee6f2c787e8b9806c9a9c969`  
		Last Modified: Fri, 16 Jan 2026 22:45:38 GMT  
		Size: 5.6 MB (5592530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa662e79d45a5b6a60edcb33a6f22188c2cfa985ed1b67ef7d9bfef7ebb21087`  
		Last Modified: Fri, 16 Jan 2026 22:45:39 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:e710e94955768bd41a14f809d4d928e15a84d8a6245cc224dc99cf2ee2338d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221405328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ddf88f39a855f8364b0c92d1913a540fc11ec7b886d770172e17cab3fbf16a`
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
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:49:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:49:57 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:50:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:53:01 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:01 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:01 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:01 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
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
	-	`sha256:a249d6508920eeaed8c936fcd9d1266903a78701d8d719939629aecacd2b3612`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 1.2 MB (1214444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cecadaf268b53180de45b75d528261de3e54e528974811d9678e3ad073280`  
		Last Modified: Fri, 16 Jan 2026 21:53:48 GMT  
		Size: 11.7 MB (11694733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df3a8008132b7222b86b8fcf41e409341df064efb15cd0b2db76a2e43652440`  
		Last Modified: Fri, 16 Jan 2026 21:55:08 GMT  
		Size: 138.6 MB (138635032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a54b4827a3677d869daa769f728f3d85ed1c41810346c406ebdba1c9d6017bb`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:bbd9199cb4a5da33fb05a2c105163173092e1633d862b6c8b4709cf5dc9283e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5621812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b6b5679fb62f0751fd471ebda0daf079057a1d2440fb4f139bd37db503a5cb`

```dockerfile
```

-	Layers:
	-	`sha256:ecc780399baa396908b03e0e41b891f1866a69664c910d13f5c8f6839801370a`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 5.6 MB (5595327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b857b5e875c2615f4e29809571a4619dc21beb25493216bedf4002027ac0ab97`  
		Last Modified: Fri, 16 Jan 2026 22:45:45 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cd23414049a2774d17ae2dd1e327e1037e2ae277751e37e06a25cd0da6a35a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230013156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1383692cd7c356a7a82172e9a8f64527070c1550ab468edb794c3ecc7e285d09`
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
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:29 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:06 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:06 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:06 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87c15c864725a8daa5ca1505d5d886e53928b49fa578e7a35dc51a4be5b715d`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4c74fb4662b26fe96702c59c427e26bd0489a0a1c1c5960592b029426583e3`  
		Last Modified: Wed, 14 Jan 2026 18:01:50 GMT  
		Size: 49.6 MB (49611029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20454c8e368d7849b8d2669b17f01d47585f0d71a5b683c0c03997c8733f81d2`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 1.7 MB (1712623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6686bd0124e3e3612ac03ec0e58e60f1d86a689763f36ecade62f90a4f8d1ea`  
		Last Modified: Wed, 14 Jan 2026 18:01:49 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7033eb962607a955c6372a69ee5257aa923a8d39d76674bd162f2787d935f3a`  
		Last Modified: Fri, 16 Jan 2026 21:54:44 GMT  
		Size: 1.2 MB (1201530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7651bda82d46538be346d839ca10addf26d82eede645b669e55ce70b5f63385`  
		Last Modified: Fri, 16 Jan 2026 21:54:54 GMT  
		Size: 11.7 MB (11703412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc9b9f0753a93ea6ffa5029194830560b1d152496a86a2b86054592ebe5a0c3`  
		Last Modified: Fri, 16 Jan 2026 21:54:47 GMT  
		Size: 137.7 MB (137672344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd6c458dda55df446dcb602d8173c61779b73d3a0ccbf96b3ec524e423e9d3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:53 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:02e7bd8415afbd519cd16da0a7c5f58bed487547a747c2962e0a62f6fd97b13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5619410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834af9f6d47a9d1a26e9c3b13c3ff24c2bf447846c1f4deb20f4a369ccbaae4f`

```dockerfile
```

-	Layers:
	-	`sha256:0ddf820b5a6704d55ee73e6166e8dc592df42b3892756b31e43cd02d23d23cb8`  
		Last Modified: Fri, 16 Jan 2026 22:45:51 GMT  
		Size: 5.6 MB (5592881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05df5e3594cece8c76e3b739c4668dc514e605246c00962e575600b709e88a3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:43 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:c3436627928b1b43d1456845ecbf82ba8d9e3a7e42f317f4a2a18b6a0f4dacfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231935344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43437d8327a686e5f5a504963fdc52b1d29e8051166b368362edf196278c856`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 21:22:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 21:23:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 21:23:44 GMT
CMD ["node"]
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 22:23:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 22:23:31 GMT
ENV NODE_ENV=production
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 15 Jan 2026 22:23:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:57:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:57:35 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:57:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:57:35 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:57:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d139ad9a3a58767f140c3201036e062e1a612d605a2d9ad8f971d9d78b53105`  
		Last Modified: Tue, 13 Jan 2026 02:16:16 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b8ffadc3140bf38490474eefe010b5d358986aad8d44529804b0743054faac`  
		Last Modified: Wed, 14 Jan 2026 21:24:32 GMT  
		Size: 49.7 MB (49677854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d962a7944bc35ac4232287b29129631cb30e0c2303fe9accd5060e13d10e417c`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 1.7 MB (1713059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b2eef94eee0b83f1a3d7a9599195e40b2dc80c3676e1214811bd87d43ba5c6`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9743a6eb0019afb918d9a783e9824fd189d217337fdd105c51b13324597390`  
		Last Modified: Thu, 15 Jan 2026 23:29:01 GMT  
		Size: 1.2 MB (1221797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dc1783fd9f5092bf435b4a7176f1ffa2e2a22e9cb73e36790448ef519cc84d`  
		Last Modified: Thu, 15 Jan 2026 22:27:23 GMT  
		Size: 11.7 MB (11713708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad56df80bd6319c74dfc884bd19c872678904e3b83a9172205691d51dccf11b`  
		Last Modified: Fri, 16 Jan 2026 21:58:54 GMT  
		Size: 140.7 MB (140720181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d310d3c0fa29617bb1c71502f8aa26ec106e911099b6ead0f3fe978b9fe79f3`  
		Last Modified: Fri, 16 Jan 2026 21:58:39 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:77c6a5256641362cf56117a966d9303ba1632d8372901ae78527d59d41ecb9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4c08dd2b8bd5bdf1989895beb8d39f88a2f595895b66edf7aad20ffbd6cf2e`

```dockerfile
```

-	Layers:
	-	`sha256:8bd1303d556029148a7040fb1ec53ec847e4cb6d399044f8f4b7e982cf607135`  
		Last Modified: Fri, 16 Jan 2026 21:58:30 GMT  
		Size: 5.6 MB (5586355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d098d8ceb9e37f70da4e29e97439abe0305c8aadae217d3666565b2e120f8e14`  
		Last Modified: Fri, 16 Jan 2026 22:45:59 GMT  
		Size: 26.3 KB (26346 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.13.2`

```console
$ docker pull ghost@sha256:86090f3ee57af8d8e3fa11875b5787068a1c17b8aebd4b88d932efe11097f578
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

### `ghost:6.13.2` - linux; amd64

```console
$ docker pull ghost@sha256:ef3782910d75e1a4d0f2fee23d521f47ff4f2dd770a00d6cb4bd5a45c260165d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229949562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e67eca0fbe174babbedbd2b2dab2f54beefaf217dfe3b076edb2941c72d4181`
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
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:51 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:00 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:00 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:00 GMT
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
		Last Modified: Wed, 14 Jan 2026 17:59:37 GMT  
		Size: 49.5 MB (49472719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ac2b87b09265a60e104e3d87872d2c15f913cbbfd4d401b5e4b5353e4ced4`  
		Last Modified: Wed, 14 Jan 2026 17:59:48 GMT  
		Size: 1.7 MB (1712660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cc9ecead9d0fe8970f3923a484fcd4fe1fd027fab911d462ca552cd57d5dbf`  
		Last Modified: Wed, 14 Jan 2026 17:59:36 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d9069be84eda409daf000052287ded0488fa41932b208a91d7b5d9c61fb1db`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 1.2 MB (1247544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139dd34f662903c210b176797936f46c21e51067027a573dba8cf698eec3198`  
		Last Modified: Fri, 16 Jan 2026 21:53:42 GMT  
		Size: 11.7 MB (11704039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe03f721169025219aa078337a2541219c5ac7246fb867e8aff113d1e20b884`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 137.6 MB (137579701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54048a9e0fb4911913295adb6af4358c80b7065fbed3847c9f8896df95c8853`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13.2` - unknown; unknown

```console
$ docker pull ghost@sha256:f0a051f5af0b039dad919753c3041d11088d11264a2d6b34202496fa65ceea68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5618877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aec6fe309a03ace913e95d0b5789af60ff41dc0a6518a6701233a74996e75f8`

```dockerfile
```

-	Layers:
	-	`sha256:939d78f65f1ccf8a812605765fcd939e938d2218ee6f2c787e8b9806c9a9c969`  
		Last Modified: Fri, 16 Jan 2026 22:45:38 GMT  
		Size: 5.6 MB (5592530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa662e79d45a5b6a60edcb33a6f22188c2cfa985ed1b67ef7d9bfef7ebb21087`  
		Last Modified: Fri, 16 Jan 2026 22:45:39 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13.2` - linux; arm variant v7

```console
$ docker pull ghost@sha256:e710e94955768bd41a14f809d4d928e15a84d8a6245cc224dc99cf2ee2338d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221405328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ddf88f39a855f8364b0c92d1913a540fc11ec7b886d770172e17cab3fbf16a`
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
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:49:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:49:57 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:50:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:53:01 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:01 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:01 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:01 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
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
	-	`sha256:a249d6508920eeaed8c936fcd9d1266903a78701d8d719939629aecacd2b3612`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 1.2 MB (1214444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cecadaf268b53180de45b75d528261de3e54e528974811d9678e3ad073280`  
		Last Modified: Fri, 16 Jan 2026 21:53:48 GMT  
		Size: 11.7 MB (11694733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df3a8008132b7222b86b8fcf41e409341df064efb15cd0b2db76a2e43652440`  
		Last Modified: Fri, 16 Jan 2026 21:55:08 GMT  
		Size: 138.6 MB (138635032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a54b4827a3677d869daa769f728f3d85ed1c41810346c406ebdba1c9d6017bb`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13.2` - unknown; unknown

```console
$ docker pull ghost@sha256:bbd9199cb4a5da33fb05a2c105163173092e1633d862b6c8b4709cf5dc9283e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5621812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b6b5679fb62f0751fd471ebda0daf079057a1d2440fb4f139bd37db503a5cb`

```dockerfile
```

-	Layers:
	-	`sha256:ecc780399baa396908b03e0e41b891f1866a69664c910d13f5c8f6839801370a`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 5.6 MB (5595327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b857b5e875c2615f4e29809571a4619dc21beb25493216bedf4002027ac0ab97`  
		Last Modified: Fri, 16 Jan 2026 22:45:45 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13.2` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cd23414049a2774d17ae2dd1e327e1037e2ae277751e37e06a25cd0da6a35a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230013156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1383692cd7c356a7a82172e9a8f64527070c1550ab468edb794c3ecc7e285d09`
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
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:29 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:06 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:06 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:06 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87c15c864725a8daa5ca1505d5d886e53928b49fa578e7a35dc51a4be5b715d`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4c74fb4662b26fe96702c59c427e26bd0489a0a1c1c5960592b029426583e3`  
		Last Modified: Wed, 14 Jan 2026 18:01:50 GMT  
		Size: 49.6 MB (49611029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20454c8e368d7849b8d2669b17f01d47585f0d71a5b683c0c03997c8733f81d2`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 1.7 MB (1712623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6686bd0124e3e3612ac03ec0e58e60f1d86a689763f36ecade62f90a4f8d1ea`  
		Last Modified: Wed, 14 Jan 2026 18:01:49 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7033eb962607a955c6372a69ee5257aa923a8d39d76674bd162f2787d935f3a`  
		Last Modified: Fri, 16 Jan 2026 21:54:44 GMT  
		Size: 1.2 MB (1201530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7651bda82d46538be346d839ca10addf26d82eede645b669e55ce70b5f63385`  
		Last Modified: Fri, 16 Jan 2026 21:54:54 GMT  
		Size: 11.7 MB (11703412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc9b9f0753a93ea6ffa5029194830560b1d152496a86a2b86054592ebe5a0c3`  
		Last Modified: Fri, 16 Jan 2026 21:54:47 GMT  
		Size: 137.7 MB (137672344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd6c458dda55df446dcb602d8173c61779b73d3a0ccbf96b3ec524e423e9d3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:53 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13.2` - unknown; unknown

```console
$ docker pull ghost@sha256:02e7bd8415afbd519cd16da0a7c5f58bed487547a747c2962e0a62f6fd97b13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5619410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834af9f6d47a9d1a26e9c3b13c3ff24c2bf447846c1f4deb20f4a369ccbaae4f`

```dockerfile
```

-	Layers:
	-	`sha256:0ddf820b5a6704d55ee73e6166e8dc592df42b3892756b31e43cd02d23d23cb8`  
		Last Modified: Fri, 16 Jan 2026 22:45:51 GMT  
		Size: 5.6 MB (5592881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05df5e3594cece8c76e3b739c4668dc514e605246c00962e575600b709e88a3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:43 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13.2` - linux; s390x

```console
$ docker pull ghost@sha256:c3436627928b1b43d1456845ecbf82ba8d9e3a7e42f317f4a2a18b6a0f4dacfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231935344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43437d8327a686e5f5a504963fdc52b1d29e8051166b368362edf196278c856`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 21:22:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 21:23:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 21:23:44 GMT
CMD ["node"]
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 22:23:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 22:23:31 GMT
ENV NODE_ENV=production
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 15 Jan 2026 22:23:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:57:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:57:35 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:57:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:57:35 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:57:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d139ad9a3a58767f140c3201036e062e1a612d605a2d9ad8f971d9d78b53105`  
		Last Modified: Tue, 13 Jan 2026 02:16:16 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b8ffadc3140bf38490474eefe010b5d358986aad8d44529804b0743054faac`  
		Last Modified: Wed, 14 Jan 2026 21:24:32 GMT  
		Size: 49.7 MB (49677854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d962a7944bc35ac4232287b29129631cb30e0c2303fe9accd5060e13d10e417c`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 1.7 MB (1713059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b2eef94eee0b83f1a3d7a9599195e40b2dc80c3676e1214811bd87d43ba5c6`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9743a6eb0019afb918d9a783e9824fd189d217337fdd105c51b13324597390`  
		Last Modified: Thu, 15 Jan 2026 23:29:01 GMT  
		Size: 1.2 MB (1221797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dc1783fd9f5092bf435b4a7176f1ffa2e2a22e9cb73e36790448ef519cc84d`  
		Last Modified: Thu, 15 Jan 2026 22:27:23 GMT  
		Size: 11.7 MB (11713708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad56df80bd6319c74dfc884bd19c872678904e3b83a9172205691d51dccf11b`  
		Last Modified: Fri, 16 Jan 2026 21:58:54 GMT  
		Size: 140.7 MB (140720181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d310d3c0fa29617bb1c71502f8aa26ec106e911099b6ead0f3fe978b9fe79f3`  
		Last Modified: Fri, 16 Jan 2026 21:58:39 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13.2` - unknown; unknown

```console
$ docker pull ghost@sha256:77c6a5256641362cf56117a966d9303ba1632d8372901ae78527d59d41ecb9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4c08dd2b8bd5bdf1989895beb8d39f88a2f595895b66edf7aad20ffbd6cf2e`

```dockerfile
```

-	Layers:
	-	`sha256:8bd1303d556029148a7040fb1ec53ec847e4cb6d399044f8f4b7e982cf607135`  
		Last Modified: Fri, 16 Jan 2026 21:58:30 GMT  
		Size: 5.6 MB (5586355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d098d8ceb9e37f70da4e29e97439abe0305c8aadae217d3666565b2e120f8e14`  
		Last Modified: Fri, 16 Jan 2026 22:45:59 GMT  
		Size: 26.3 KB (26346 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.13.2-alpine`

```console
$ docker pull ghost@sha256:914e79639c3335775a3963897909c183751a4639c069f6a686b1f3ce634d87ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.13.2-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:17e5b1f5af110967679bf1396274c9f0230c12181a1b368028e30386c5523ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207580257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f321510e4d3eeefe9b778c2db896377c50f4fbd9b3d8839ad461f39258d4ec30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:58:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 17:58:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:58:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:59:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:59:03 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:50:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:04 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:57 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:52:58 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:52:58 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:52:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dda044491a389c13d0aa53e5cc14375121749b7401b4db1825fd97191528aa`  
		Last Modified: Wed, 14 Jan 2026 17:59:34 GMT  
		Size: 51.6 MB (51601845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5453a6a95efdb1bc3321878ea844e2c518f39aecd5f7f8a78e1b78d89a637e`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 1.3 MB (1262129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd007ec038c44249b9612b09663aa39b77c77bf71eeed265f47bf14154bce59c`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a042a68d544d0e6e4af4122ae40be7b77648d26905a2090b25bc7494bbb22840`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 821.9 KB (821904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153d1b71d487941b613e2eae005aabdf6f1626041fd953b1bad75dcd1bb5a5ec`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 928.3 KB (928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd27759c78d3456cb0a43fdcce8bc5257f49e71e5fac8bee7760338bf5947d1`  
		Last Modified: Fri, 16 Jan 2026 21:53:28 GMT  
		Size: 11.7 MB (11704085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f498c381e2c67fe0c5122d9a9e1c76d3b94b4a927da0a2d03229db33994733e`  
		Last Modified: Fri, 16 Jan 2026 21:53:31 GMT  
		Size: 137.4 MB (137400829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04924f1eec39098092b680ae31e7c72b272d50f5e6fb85e6f3ae274fc5c9068`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13.2-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:a6c58b116386808827fae97b5cd4e4c369ccf8b0258ad7dd69e44d05cd6f4731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f2ec9918f583fccf6f21998f4f167e2a58ac920a836ac0505558d6b0390f0b`

```dockerfile
```

-	Layers:
	-	`sha256:13a8e432a2560ff262b164884933a7f97e6393fbfe9e855827e44dd85fbc4aa6`  
		Last Modified: Fri, 16 Jan 2026 22:45:47 GMT  
		Size: 3.4 MB (3380529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bcb20062eda86d699ac09b7c815241e18aad84beb68635a2f40175751eeb5f8`  
		Last Modified: Fri, 16 Jan 2026 22:45:48 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13.2-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:56ca8e2e13d8384c602992ed334702c2ac15eb010d0d8dccd3b2f6a71a0067cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219446765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c2373454f0661e9b0ee88181e279d0134dc3bc9d86e612eecbecee29089148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:28:46 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 18:28:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:46 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:28:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:28:49 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:51:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:37 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:29 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:29 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:29 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88a575fc12781c98ff7a5b3d03ea1b36814176fddaf1e55e0b1bb14bc6c34e4`  
		Last Modified: Wed, 14 Jan 2026 18:29:25 GMT  
		Size: 52.2 MB (52237556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8623286f7776425bdee32d428d0c53f4acc0d836ec7ac19fff597b59095a9e`  
		Last Modified: Wed, 14 Jan 2026 18:29:14 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed93f8843f88facc599516714a1f82921aa4778c5fec480d0e4ab5410c54695`  
		Last Modified: Wed, 14 Jan 2026 18:29:04 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306c771ee35c6cec4a540617727df3f40b9a5c232a5a4094a4bf72dbbd4f4f61`  
		Last Modified: Fri, 16 Jan 2026 21:55:18 GMT  
		Size: 891.3 KB (891301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9733ede21bc1c0310cf194d38777508c5427c1e9f9fd6d6443208b1c07ad3a8c`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 881.3 KB (881291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a638dd4f153662af93a01c15f7b866acc2fa88d5160b92b317699d9ff56ef2ce`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 11.7 MB (11703289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dab10d9a81f61bdd780ff327a8d1d829b8b2f4babeb70aa93cc854881b1c91a`  
		Last Modified: Fri, 16 Jan 2026 21:55:10 GMT  
		Size: 148.3 MB (148273578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a7bc6e0a1ffaf5fb2be6585bba15cd3bcf026dc6794580f0b5b03a090125d4`  
		Last Modified: Fri, 16 Jan 2026 21:55:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13.2-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:be3ff6e8c6c43594c2e6f87aa27c1afe2a96a01d0537ee1200f269baf1e72814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29859ce48bfbb7b6978182944457e7c0209806800411d1da893a96a7a06ee01`

```dockerfile
```

-	Layers:
	-	`sha256:5f9331badabe199f703be07f013eea0245f7b3da4bc86518f347d46dd0a52707`  
		Last Modified: Fri, 16 Jan 2026 22:45:53 GMT  
		Size: 3.4 MB (3380035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c33f5ddc0479111797b425a08e20e85f80919522a33eba654bb5d229b194b2`  
		Last Modified: Fri, 16 Jan 2026 22:45:54 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.13.2-alpine3.23`

```console
$ docker pull ghost@sha256:914e79639c3335775a3963897909c183751a4639c069f6a686b1f3ce634d87ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.13.2-alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:17e5b1f5af110967679bf1396274c9f0230c12181a1b368028e30386c5523ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207580257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f321510e4d3eeefe9b778c2db896377c50f4fbd9b3d8839ad461f39258d4ec30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:58:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 17:58:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:58:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:59:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:59:03 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:50:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:04 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:57 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:52:58 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:52:58 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:52:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dda044491a389c13d0aa53e5cc14375121749b7401b4db1825fd97191528aa`  
		Last Modified: Wed, 14 Jan 2026 17:59:34 GMT  
		Size: 51.6 MB (51601845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5453a6a95efdb1bc3321878ea844e2c518f39aecd5f7f8a78e1b78d89a637e`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 1.3 MB (1262129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd007ec038c44249b9612b09663aa39b77c77bf71eeed265f47bf14154bce59c`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a042a68d544d0e6e4af4122ae40be7b77648d26905a2090b25bc7494bbb22840`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 821.9 KB (821904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153d1b71d487941b613e2eae005aabdf6f1626041fd953b1bad75dcd1bb5a5ec`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 928.3 KB (928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd27759c78d3456cb0a43fdcce8bc5257f49e71e5fac8bee7760338bf5947d1`  
		Last Modified: Fri, 16 Jan 2026 21:53:28 GMT  
		Size: 11.7 MB (11704085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f498c381e2c67fe0c5122d9a9e1c76d3b94b4a927da0a2d03229db33994733e`  
		Last Modified: Fri, 16 Jan 2026 21:53:31 GMT  
		Size: 137.4 MB (137400829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04924f1eec39098092b680ae31e7c72b272d50f5e6fb85e6f3ae274fc5c9068`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13.2-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:a6c58b116386808827fae97b5cd4e4c369ccf8b0258ad7dd69e44d05cd6f4731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f2ec9918f583fccf6f21998f4f167e2a58ac920a836ac0505558d6b0390f0b`

```dockerfile
```

-	Layers:
	-	`sha256:13a8e432a2560ff262b164884933a7f97e6393fbfe9e855827e44dd85fbc4aa6`  
		Last Modified: Fri, 16 Jan 2026 22:45:47 GMT  
		Size: 3.4 MB (3380529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bcb20062eda86d699ac09b7c815241e18aad84beb68635a2f40175751eeb5f8`  
		Last Modified: Fri, 16 Jan 2026 22:45:48 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13.2-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:56ca8e2e13d8384c602992ed334702c2ac15eb010d0d8dccd3b2f6a71a0067cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219446765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c2373454f0661e9b0ee88181e279d0134dc3bc9d86e612eecbecee29089148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:28:46 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 18:28:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:46 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:28:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:28:49 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:51:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:37 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:29 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:29 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:29 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88a575fc12781c98ff7a5b3d03ea1b36814176fddaf1e55e0b1bb14bc6c34e4`  
		Last Modified: Wed, 14 Jan 2026 18:29:25 GMT  
		Size: 52.2 MB (52237556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8623286f7776425bdee32d428d0c53f4acc0d836ec7ac19fff597b59095a9e`  
		Last Modified: Wed, 14 Jan 2026 18:29:14 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed93f8843f88facc599516714a1f82921aa4778c5fec480d0e4ab5410c54695`  
		Last Modified: Wed, 14 Jan 2026 18:29:04 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306c771ee35c6cec4a540617727df3f40b9a5c232a5a4094a4bf72dbbd4f4f61`  
		Last Modified: Fri, 16 Jan 2026 21:55:18 GMT  
		Size: 891.3 KB (891301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9733ede21bc1c0310cf194d38777508c5427c1e9f9fd6d6443208b1c07ad3a8c`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 881.3 KB (881291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a638dd4f153662af93a01c15f7b866acc2fa88d5160b92b317699d9ff56ef2ce`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 11.7 MB (11703289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dab10d9a81f61bdd780ff327a8d1d829b8b2f4babeb70aa93cc854881b1c91a`  
		Last Modified: Fri, 16 Jan 2026 21:55:10 GMT  
		Size: 148.3 MB (148273578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a7bc6e0a1ffaf5fb2be6585bba15cd3bcf026dc6794580f0b5b03a090125d4`  
		Last Modified: Fri, 16 Jan 2026 21:55:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13.2-alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:be3ff6e8c6c43594c2e6f87aa27c1afe2a96a01d0537ee1200f269baf1e72814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29859ce48bfbb7b6978182944457e7c0209806800411d1da893a96a7a06ee01`

```dockerfile
```

-	Layers:
	-	`sha256:5f9331badabe199f703be07f013eea0245f7b3da4bc86518f347d46dd0a52707`  
		Last Modified: Fri, 16 Jan 2026 22:45:53 GMT  
		Size: 3.4 MB (3380035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c33f5ddc0479111797b425a08e20e85f80919522a33eba654bb5d229b194b2`  
		Last Modified: Fri, 16 Jan 2026 22:45:54 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.13.2-bookworm`

```console
$ docker pull ghost@sha256:86090f3ee57af8d8e3fa11875b5787068a1c17b8aebd4b88d932efe11097f578
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

### `ghost:6.13.2-bookworm` - linux; amd64

```console
$ docker pull ghost@sha256:ef3782910d75e1a4d0f2fee23d521f47ff4f2dd770a00d6cb4bd5a45c260165d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229949562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e67eca0fbe174babbedbd2b2dab2f54beefaf217dfe3b076edb2941c72d4181`
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
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:51 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:00 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:00 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:00 GMT
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
		Last Modified: Wed, 14 Jan 2026 17:59:37 GMT  
		Size: 49.5 MB (49472719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ac2b87b09265a60e104e3d87872d2c15f913cbbfd4d401b5e4b5353e4ced4`  
		Last Modified: Wed, 14 Jan 2026 17:59:48 GMT  
		Size: 1.7 MB (1712660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cc9ecead9d0fe8970f3923a484fcd4fe1fd027fab911d462ca552cd57d5dbf`  
		Last Modified: Wed, 14 Jan 2026 17:59:36 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d9069be84eda409daf000052287ded0488fa41932b208a91d7b5d9c61fb1db`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 1.2 MB (1247544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139dd34f662903c210b176797936f46c21e51067027a573dba8cf698eec3198`  
		Last Modified: Fri, 16 Jan 2026 21:53:42 GMT  
		Size: 11.7 MB (11704039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe03f721169025219aa078337a2541219c5ac7246fb867e8aff113d1e20b884`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 137.6 MB (137579701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54048a9e0fb4911913295adb6af4358c80b7065fbed3847c9f8896df95c8853`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13.2-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:f0a051f5af0b039dad919753c3041d11088d11264a2d6b34202496fa65ceea68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5618877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aec6fe309a03ace913e95d0b5789af60ff41dc0a6518a6701233a74996e75f8`

```dockerfile
```

-	Layers:
	-	`sha256:939d78f65f1ccf8a812605765fcd939e938d2218ee6f2c787e8b9806c9a9c969`  
		Last Modified: Fri, 16 Jan 2026 22:45:38 GMT  
		Size: 5.6 MB (5592530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa662e79d45a5b6a60edcb33a6f22188c2cfa985ed1b67ef7d9bfef7ebb21087`  
		Last Modified: Fri, 16 Jan 2026 22:45:39 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13.2-bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:e710e94955768bd41a14f809d4d928e15a84d8a6245cc224dc99cf2ee2338d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221405328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ddf88f39a855f8364b0c92d1913a540fc11ec7b886d770172e17cab3fbf16a`
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
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:49:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:49:57 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:50:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:53:01 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:01 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:01 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:01 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
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
	-	`sha256:a249d6508920eeaed8c936fcd9d1266903a78701d8d719939629aecacd2b3612`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 1.2 MB (1214444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cecadaf268b53180de45b75d528261de3e54e528974811d9678e3ad073280`  
		Last Modified: Fri, 16 Jan 2026 21:53:48 GMT  
		Size: 11.7 MB (11694733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df3a8008132b7222b86b8fcf41e409341df064efb15cd0b2db76a2e43652440`  
		Last Modified: Fri, 16 Jan 2026 21:55:08 GMT  
		Size: 138.6 MB (138635032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a54b4827a3677d869daa769f728f3d85ed1c41810346c406ebdba1c9d6017bb`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13.2-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:bbd9199cb4a5da33fb05a2c105163173092e1633d862b6c8b4709cf5dc9283e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5621812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b6b5679fb62f0751fd471ebda0daf079057a1d2440fb4f139bd37db503a5cb`

```dockerfile
```

-	Layers:
	-	`sha256:ecc780399baa396908b03e0e41b891f1866a69664c910d13f5c8f6839801370a`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 5.6 MB (5595327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b857b5e875c2615f4e29809571a4619dc21beb25493216bedf4002027ac0ab97`  
		Last Modified: Fri, 16 Jan 2026 22:45:45 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cd23414049a2774d17ae2dd1e327e1037e2ae277751e37e06a25cd0da6a35a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230013156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1383692cd7c356a7a82172e9a8f64527070c1550ab468edb794c3ecc7e285d09`
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
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:29 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:06 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:06 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:06 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87c15c864725a8daa5ca1505d5d886e53928b49fa578e7a35dc51a4be5b715d`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4c74fb4662b26fe96702c59c427e26bd0489a0a1c1c5960592b029426583e3`  
		Last Modified: Wed, 14 Jan 2026 18:01:50 GMT  
		Size: 49.6 MB (49611029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20454c8e368d7849b8d2669b17f01d47585f0d71a5b683c0c03997c8733f81d2`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 1.7 MB (1712623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6686bd0124e3e3612ac03ec0e58e60f1d86a689763f36ecade62f90a4f8d1ea`  
		Last Modified: Wed, 14 Jan 2026 18:01:49 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7033eb962607a955c6372a69ee5257aa923a8d39d76674bd162f2787d935f3a`  
		Last Modified: Fri, 16 Jan 2026 21:54:44 GMT  
		Size: 1.2 MB (1201530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7651bda82d46538be346d839ca10addf26d82eede645b669e55ce70b5f63385`  
		Last Modified: Fri, 16 Jan 2026 21:54:54 GMT  
		Size: 11.7 MB (11703412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc9b9f0753a93ea6ffa5029194830560b1d152496a86a2b86054592ebe5a0c3`  
		Last Modified: Fri, 16 Jan 2026 21:54:47 GMT  
		Size: 137.7 MB (137672344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd6c458dda55df446dcb602d8173c61779b73d3a0ccbf96b3ec524e423e9d3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:53 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13.2-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:02e7bd8415afbd519cd16da0a7c5f58bed487547a747c2962e0a62f6fd97b13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5619410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834af9f6d47a9d1a26e9c3b13c3ff24c2bf447846c1f4deb20f4a369ccbaae4f`

```dockerfile
```

-	Layers:
	-	`sha256:0ddf820b5a6704d55ee73e6166e8dc592df42b3892756b31e43cd02d23d23cb8`  
		Last Modified: Fri, 16 Jan 2026 22:45:51 GMT  
		Size: 5.6 MB (5592881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05df5e3594cece8c76e3b739c4668dc514e605246c00962e575600b709e88a3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:43 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.13.2-bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:c3436627928b1b43d1456845ecbf82ba8d9e3a7e42f317f4a2a18b6a0f4dacfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231935344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43437d8327a686e5f5a504963fdc52b1d29e8051166b368362edf196278c856`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 21:22:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 21:23:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 21:23:44 GMT
CMD ["node"]
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 22:23:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 22:23:31 GMT
ENV NODE_ENV=production
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 15 Jan 2026 22:23:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:57:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:57:35 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:57:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:57:35 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:57:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d139ad9a3a58767f140c3201036e062e1a612d605a2d9ad8f971d9d78b53105`  
		Last Modified: Tue, 13 Jan 2026 02:16:16 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b8ffadc3140bf38490474eefe010b5d358986aad8d44529804b0743054faac`  
		Last Modified: Wed, 14 Jan 2026 21:24:32 GMT  
		Size: 49.7 MB (49677854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d962a7944bc35ac4232287b29129631cb30e0c2303fe9accd5060e13d10e417c`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 1.7 MB (1713059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b2eef94eee0b83f1a3d7a9599195e40b2dc80c3676e1214811bd87d43ba5c6`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9743a6eb0019afb918d9a783e9824fd189d217337fdd105c51b13324597390`  
		Last Modified: Thu, 15 Jan 2026 23:29:01 GMT  
		Size: 1.2 MB (1221797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dc1783fd9f5092bf435b4a7176f1ffa2e2a22e9cb73e36790448ef519cc84d`  
		Last Modified: Thu, 15 Jan 2026 22:27:23 GMT  
		Size: 11.7 MB (11713708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad56df80bd6319c74dfc884bd19c872678904e3b83a9172205691d51dccf11b`  
		Last Modified: Fri, 16 Jan 2026 21:58:54 GMT  
		Size: 140.7 MB (140720181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d310d3c0fa29617bb1c71502f8aa26ec106e911099b6ead0f3fe978b9fe79f3`  
		Last Modified: Fri, 16 Jan 2026 21:58:39 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.13.2-bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:77c6a5256641362cf56117a966d9303ba1632d8372901ae78527d59d41ecb9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4c08dd2b8bd5bdf1989895beb8d39f88a2f595895b66edf7aad20ffbd6cf2e`

```dockerfile
```

-	Layers:
	-	`sha256:8bd1303d556029148a7040fb1ec53ec847e4cb6d399044f8f4b7e982cf607135`  
		Last Modified: Fri, 16 Jan 2026 21:58:30 GMT  
		Size: 5.6 MB (5586355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d098d8ceb9e37f70da4e29e97439abe0305c8aadae217d3666565b2e120f8e14`  
		Last Modified: Fri, 16 Jan 2026 22:45:59 GMT  
		Size: 26.3 KB (26346 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine`

```console
$ docker pull ghost@sha256:914e79639c3335775a3963897909c183751a4639c069f6a686b1f3ce634d87ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:17e5b1f5af110967679bf1396274c9f0230c12181a1b368028e30386c5523ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207580257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f321510e4d3eeefe9b778c2db896377c50f4fbd9b3d8839ad461f39258d4ec30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:58:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 17:58:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:58:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:59:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:59:03 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:50:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:04 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:57 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:52:58 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:52:58 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:52:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dda044491a389c13d0aa53e5cc14375121749b7401b4db1825fd97191528aa`  
		Last Modified: Wed, 14 Jan 2026 17:59:34 GMT  
		Size: 51.6 MB (51601845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5453a6a95efdb1bc3321878ea844e2c518f39aecd5f7f8a78e1b78d89a637e`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 1.3 MB (1262129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd007ec038c44249b9612b09663aa39b77c77bf71eeed265f47bf14154bce59c`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a042a68d544d0e6e4af4122ae40be7b77648d26905a2090b25bc7494bbb22840`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 821.9 KB (821904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153d1b71d487941b613e2eae005aabdf6f1626041fd953b1bad75dcd1bb5a5ec`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 928.3 KB (928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd27759c78d3456cb0a43fdcce8bc5257f49e71e5fac8bee7760338bf5947d1`  
		Last Modified: Fri, 16 Jan 2026 21:53:28 GMT  
		Size: 11.7 MB (11704085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f498c381e2c67fe0c5122d9a9e1c76d3b94b4a927da0a2d03229db33994733e`  
		Last Modified: Fri, 16 Jan 2026 21:53:31 GMT  
		Size: 137.4 MB (137400829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04924f1eec39098092b680ae31e7c72b272d50f5e6fb85e6f3ae274fc5c9068`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:a6c58b116386808827fae97b5cd4e4c369ccf8b0258ad7dd69e44d05cd6f4731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f2ec9918f583fccf6f21998f4f167e2a58ac920a836ac0505558d6b0390f0b`

```dockerfile
```

-	Layers:
	-	`sha256:13a8e432a2560ff262b164884933a7f97e6393fbfe9e855827e44dd85fbc4aa6`  
		Last Modified: Fri, 16 Jan 2026 22:45:47 GMT  
		Size: 3.4 MB (3380529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bcb20062eda86d699ac09b7c815241e18aad84beb68635a2f40175751eeb5f8`  
		Last Modified: Fri, 16 Jan 2026 22:45:48 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:56ca8e2e13d8384c602992ed334702c2ac15eb010d0d8dccd3b2f6a71a0067cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219446765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c2373454f0661e9b0ee88181e279d0134dc3bc9d86e612eecbecee29089148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:28:46 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 18:28:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:46 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:28:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:28:49 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:51:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:37 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:29 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:29 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:29 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88a575fc12781c98ff7a5b3d03ea1b36814176fddaf1e55e0b1bb14bc6c34e4`  
		Last Modified: Wed, 14 Jan 2026 18:29:25 GMT  
		Size: 52.2 MB (52237556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8623286f7776425bdee32d428d0c53f4acc0d836ec7ac19fff597b59095a9e`  
		Last Modified: Wed, 14 Jan 2026 18:29:14 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed93f8843f88facc599516714a1f82921aa4778c5fec480d0e4ab5410c54695`  
		Last Modified: Wed, 14 Jan 2026 18:29:04 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306c771ee35c6cec4a540617727df3f40b9a5c232a5a4094a4bf72dbbd4f4f61`  
		Last Modified: Fri, 16 Jan 2026 21:55:18 GMT  
		Size: 891.3 KB (891301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9733ede21bc1c0310cf194d38777508c5427c1e9f9fd6d6443208b1c07ad3a8c`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 881.3 KB (881291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a638dd4f153662af93a01c15f7b866acc2fa88d5160b92b317699d9ff56ef2ce`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 11.7 MB (11703289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dab10d9a81f61bdd780ff327a8d1d829b8b2f4babeb70aa93cc854881b1c91a`  
		Last Modified: Fri, 16 Jan 2026 21:55:10 GMT  
		Size: 148.3 MB (148273578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a7bc6e0a1ffaf5fb2be6585bba15cd3bcf026dc6794580f0b5b03a090125d4`  
		Last Modified: Fri, 16 Jan 2026 21:55:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:be3ff6e8c6c43594c2e6f87aa27c1afe2a96a01d0537ee1200f269baf1e72814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29859ce48bfbb7b6978182944457e7c0209806800411d1da893a96a7a06ee01`

```dockerfile
```

-	Layers:
	-	`sha256:5f9331badabe199f703be07f013eea0245f7b3da4bc86518f347d46dd0a52707`  
		Last Modified: Fri, 16 Jan 2026 22:45:53 GMT  
		Size: 3.4 MB (3380035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c33f5ddc0479111797b425a08e20e85f80919522a33eba654bb5d229b194b2`  
		Last Modified: Fri, 16 Jan 2026 22:45:54 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine3.23`

```console
$ docker pull ghost@sha256:914e79639c3335775a3963897909c183751a4639c069f6a686b1f3ce634d87ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine3.23` - linux; amd64

```console
$ docker pull ghost@sha256:17e5b1f5af110967679bf1396274c9f0230c12181a1b368028e30386c5523ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207580257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f321510e4d3eeefe9b778c2db896377c50f4fbd9b3d8839ad461f39258d4ec30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 17:58:59 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 17:58:59 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:58:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 17:59:02 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 17:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 17:59:03 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:50:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:49 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:49 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:04 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:04 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:57 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:52:58 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:52:58 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:52:58 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dda044491a389c13d0aa53e5cc14375121749b7401b4db1825fd97191528aa`  
		Last Modified: Wed, 14 Jan 2026 17:59:34 GMT  
		Size: 51.6 MB (51601845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5453a6a95efdb1bc3321878ea844e2c518f39aecd5f7f8a78e1b78d89a637e`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 1.3 MB (1262129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd007ec038c44249b9612b09663aa39b77c77bf71eeed265f47bf14154bce59c`  
		Last Modified: Wed, 14 Jan 2026 17:59:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a042a68d544d0e6e4af4122ae40be7b77648d26905a2090b25bc7494bbb22840`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 821.9 KB (821904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153d1b71d487941b613e2eae005aabdf6f1626041fd953b1bad75dcd1bb5a5ec`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 928.3 KB (928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd27759c78d3456cb0a43fdcce8bc5257f49e71e5fac8bee7760338bf5947d1`  
		Last Modified: Fri, 16 Jan 2026 21:53:28 GMT  
		Size: 11.7 MB (11704085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f498c381e2c67fe0c5122d9a9e1c76d3b94b4a927da0a2d03229db33994733e`  
		Last Modified: Fri, 16 Jan 2026 21:53:31 GMT  
		Size: 137.4 MB (137400829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04924f1eec39098092b680ae31e7c72b272d50f5e6fb85e6f3ae274fc5c9068`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:a6c58b116386808827fae97b5cd4e4c369ccf8b0258ad7dd69e44d05cd6f4731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f2ec9918f583fccf6f21998f4f167e2a58ac920a836ac0505558d6b0390f0b`

```dockerfile
```

-	Layers:
	-	`sha256:13a8e432a2560ff262b164884933a7f97e6393fbfe9e855827e44dd85fbc4aa6`  
		Last Modified: Fri, 16 Jan 2026 22:45:47 GMT  
		Size: 3.4 MB (3380529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bcb20062eda86d699ac09b7c815241e18aad84beb68635a2f40175751eeb5f8`  
		Last Modified: Fri, 16 Jan 2026 22:45:48 GMT  
		Size: 26.4 KB (26385 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:56ca8e2e13d8384c602992ed334702c2ac15eb010d0d8dccd3b2f6a71a0067cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219446765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c2373454f0661e9b0ee88181e279d0134dc3bc9d86e612eecbecee29089148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 14 Jan 2026 18:28:46 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 18:28:46 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="5618c83f81bdf51ac7fdfdf5bd6e179c15294b10ae4af13c028a27d54a0bd780" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:46 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 18:28:49 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 18:28:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 18:28:49 GMT
CMD ["node"]
# Fri, 16 Jan 2026 21:51:19 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:21 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:21 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:37 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:37 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:28 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apk add --no-cache --virtual .build-deps-ghost g++ linux-headers make python3 py3-setuptools; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apk del --no-network .build-deps-ghost; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:29 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:29 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:29 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88a575fc12781c98ff7a5b3d03ea1b36814176fddaf1e55e0b1bb14bc6c34e4`  
		Last Modified: Wed, 14 Jan 2026 18:29:25 GMT  
		Size: 52.2 MB (52237556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8623286f7776425bdee32d428d0c53f4acc0d836ec7ac19fff597b59095a9e`  
		Last Modified: Wed, 14 Jan 2026 18:29:14 GMT  
		Size: 1.3 MB (1262992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed93f8843f88facc599516714a1f82921aa4778c5fec480d0e4ab5410c54695`  
		Last Modified: Wed, 14 Jan 2026 18:29:04 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306c771ee35c6cec4a540617727df3f40b9a5c232a5a4094a4bf72dbbd4f4f61`  
		Last Modified: Fri, 16 Jan 2026 21:55:18 GMT  
		Size: 891.3 KB (891301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9733ede21bc1c0310cf194d38777508c5427c1e9f9fd6d6443208b1c07ad3a8c`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 881.3 KB (881291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a638dd4f153662af93a01c15f7b866acc2fa88d5160b92b317699d9ff56ef2ce`  
		Last Modified: Fri, 16 Jan 2026 21:55:17 GMT  
		Size: 11.7 MB (11703289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dab10d9a81f61bdd780ff327a8d1d829b8b2f4babeb70aa93cc854881b1c91a`  
		Last Modified: Fri, 16 Jan 2026 21:55:10 GMT  
		Size: 148.3 MB (148273578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a7bc6e0a1ffaf5fb2be6585bba15cd3bcf026dc6794580f0b5b03a090125d4`  
		Last Modified: Fri, 16 Jan 2026 21:55:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine3.23` - unknown; unknown

```console
$ docker pull ghost@sha256:be3ff6e8c6c43594c2e6f87aa27c1afe2a96a01d0537ee1200f269baf1e72814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3406617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29859ce48bfbb7b6978182944457e7c0209806800411d1da893a96a7a06ee01`

```dockerfile
```

-	Layers:
	-	`sha256:5f9331badabe199f703be07f013eea0245f7b3da4bc86518f347d46dd0a52707`  
		Last Modified: Fri, 16 Jan 2026 22:45:53 GMT  
		Size: 3.4 MB (3380035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c33f5ddc0479111797b425a08e20e85f80919522a33eba654bb5d229b194b2`  
		Last Modified: Fri, 16 Jan 2026 22:45:54 GMT  
		Size: 26.6 KB (26582 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:bookworm`

```console
$ docker pull ghost@sha256:86090f3ee57af8d8e3fa11875b5787068a1c17b8aebd4b88d932efe11097f578
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
$ docker pull ghost@sha256:ef3782910d75e1a4d0f2fee23d521f47ff4f2dd770a00d6cb4bd5a45c260165d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229949562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e67eca0fbe174babbedbd2b2dab2f54beefaf217dfe3b076edb2941c72d4181`
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
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:51 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:00 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:00 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:00 GMT
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
		Last Modified: Wed, 14 Jan 2026 17:59:37 GMT  
		Size: 49.5 MB (49472719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ac2b87b09265a60e104e3d87872d2c15f913cbbfd4d401b5e4b5353e4ced4`  
		Last Modified: Wed, 14 Jan 2026 17:59:48 GMT  
		Size: 1.7 MB (1712660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cc9ecead9d0fe8970f3923a484fcd4fe1fd027fab911d462ca552cd57d5dbf`  
		Last Modified: Wed, 14 Jan 2026 17:59:36 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d9069be84eda409daf000052287ded0488fa41932b208a91d7b5d9c61fb1db`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 1.2 MB (1247544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139dd34f662903c210b176797936f46c21e51067027a573dba8cf698eec3198`  
		Last Modified: Fri, 16 Jan 2026 21:53:42 GMT  
		Size: 11.7 MB (11704039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe03f721169025219aa078337a2541219c5ac7246fb867e8aff113d1e20b884`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 137.6 MB (137579701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54048a9e0fb4911913295adb6af4358c80b7065fbed3847c9f8896df95c8853`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:f0a051f5af0b039dad919753c3041d11088d11264a2d6b34202496fa65ceea68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5618877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aec6fe309a03ace913e95d0b5789af60ff41dc0a6518a6701233a74996e75f8`

```dockerfile
```

-	Layers:
	-	`sha256:939d78f65f1ccf8a812605765fcd939e938d2218ee6f2c787e8b9806c9a9c969`  
		Last Modified: Fri, 16 Jan 2026 22:45:38 GMT  
		Size: 5.6 MB (5592530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa662e79d45a5b6a60edcb33a6f22188c2cfa985ed1b67ef7d9bfef7ebb21087`  
		Last Modified: Fri, 16 Jan 2026 22:45:39 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm variant v7

```console
$ docker pull ghost@sha256:e710e94955768bd41a14f809d4d928e15a84d8a6245cc224dc99cf2ee2338d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221405328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ddf88f39a855f8364b0c92d1913a540fc11ec7b886d770172e17cab3fbf16a`
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
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:49:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:49:57 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:50:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:53:01 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:01 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:01 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:01 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
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
	-	`sha256:a249d6508920eeaed8c936fcd9d1266903a78701d8d719939629aecacd2b3612`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 1.2 MB (1214444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cecadaf268b53180de45b75d528261de3e54e528974811d9678e3ad073280`  
		Last Modified: Fri, 16 Jan 2026 21:53:48 GMT  
		Size: 11.7 MB (11694733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df3a8008132b7222b86b8fcf41e409341df064efb15cd0b2db76a2e43652440`  
		Last Modified: Fri, 16 Jan 2026 21:55:08 GMT  
		Size: 138.6 MB (138635032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a54b4827a3677d869daa769f728f3d85ed1c41810346c406ebdba1c9d6017bb`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:bbd9199cb4a5da33fb05a2c105163173092e1633d862b6c8b4709cf5dc9283e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5621812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b6b5679fb62f0751fd471ebda0daf079057a1d2440fb4f139bd37db503a5cb`

```dockerfile
```

-	Layers:
	-	`sha256:ecc780399baa396908b03e0e41b891f1866a69664c910d13f5c8f6839801370a`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 5.6 MB (5595327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b857b5e875c2615f4e29809571a4619dc21beb25493216bedf4002027ac0ab97`  
		Last Modified: Fri, 16 Jan 2026 22:45:45 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cd23414049a2774d17ae2dd1e327e1037e2ae277751e37e06a25cd0da6a35a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230013156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1383692cd7c356a7a82172e9a8f64527070c1550ab468edb794c3ecc7e285d09`
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
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:29 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:06 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:06 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:06 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87c15c864725a8daa5ca1505d5d886e53928b49fa578e7a35dc51a4be5b715d`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4c74fb4662b26fe96702c59c427e26bd0489a0a1c1c5960592b029426583e3`  
		Last Modified: Wed, 14 Jan 2026 18:01:50 GMT  
		Size: 49.6 MB (49611029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20454c8e368d7849b8d2669b17f01d47585f0d71a5b683c0c03997c8733f81d2`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 1.7 MB (1712623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6686bd0124e3e3612ac03ec0e58e60f1d86a689763f36ecade62f90a4f8d1ea`  
		Last Modified: Wed, 14 Jan 2026 18:01:49 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7033eb962607a955c6372a69ee5257aa923a8d39d76674bd162f2787d935f3a`  
		Last Modified: Fri, 16 Jan 2026 21:54:44 GMT  
		Size: 1.2 MB (1201530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7651bda82d46538be346d839ca10addf26d82eede645b669e55ce70b5f63385`  
		Last Modified: Fri, 16 Jan 2026 21:54:54 GMT  
		Size: 11.7 MB (11703412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc9b9f0753a93ea6ffa5029194830560b1d152496a86a2b86054592ebe5a0c3`  
		Last Modified: Fri, 16 Jan 2026 21:54:47 GMT  
		Size: 137.7 MB (137672344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd6c458dda55df446dcb602d8173c61779b73d3a0ccbf96b3ec524e423e9d3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:53 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:02e7bd8415afbd519cd16da0a7c5f58bed487547a747c2962e0a62f6fd97b13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5619410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834af9f6d47a9d1a26e9c3b13c3ff24c2bf447846c1f4deb20f4a369ccbaae4f`

```dockerfile
```

-	Layers:
	-	`sha256:0ddf820b5a6704d55ee73e6166e8dc592df42b3892756b31e43cd02d23d23cb8`  
		Last Modified: Fri, 16 Jan 2026 22:45:51 GMT  
		Size: 5.6 MB (5592881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05df5e3594cece8c76e3b739c4668dc514e605246c00962e575600b709e88a3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:43 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:bookworm` - linux; s390x

```console
$ docker pull ghost@sha256:c3436627928b1b43d1456845ecbf82ba8d9e3a7e42f317f4a2a18b6a0f4dacfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231935344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43437d8327a686e5f5a504963fdc52b1d29e8051166b368362edf196278c856`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 21:22:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 21:23:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 21:23:44 GMT
CMD ["node"]
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 22:23:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 22:23:31 GMT
ENV NODE_ENV=production
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 15 Jan 2026 22:23:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:57:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:57:35 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:57:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:57:35 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:57:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d139ad9a3a58767f140c3201036e062e1a612d605a2d9ad8f971d9d78b53105`  
		Last Modified: Tue, 13 Jan 2026 02:16:16 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b8ffadc3140bf38490474eefe010b5d358986aad8d44529804b0743054faac`  
		Last Modified: Wed, 14 Jan 2026 21:24:32 GMT  
		Size: 49.7 MB (49677854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d962a7944bc35ac4232287b29129631cb30e0c2303fe9accd5060e13d10e417c`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 1.7 MB (1713059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b2eef94eee0b83f1a3d7a9599195e40b2dc80c3676e1214811bd87d43ba5c6`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9743a6eb0019afb918d9a783e9824fd189d217337fdd105c51b13324597390`  
		Last Modified: Thu, 15 Jan 2026 23:29:01 GMT  
		Size: 1.2 MB (1221797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dc1783fd9f5092bf435b4a7176f1ffa2e2a22e9cb73e36790448ef519cc84d`  
		Last Modified: Thu, 15 Jan 2026 22:27:23 GMT  
		Size: 11.7 MB (11713708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad56df80bd6319c74dfc884bd19c872678904e3b83a9172205691d51dccf11b`  
		Last Modified: Fri, 16 Jan 2026 21:58:54 GMT  
		Size: 140.7 MB (140720181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d310d3c0fa29617bb1c71502f8aa26ec106e911099b6ead0f3fe978b9fe79f3`  
		Last Modified: Fri, 16 Jan 2026 21:58:39 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:bookworm` - unknown; unknown

```console
$ docker pull ghost@sha256:77c6a5256641362cf56117a966d9303ba1632d8372901ae78527d59d41ecb9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4c08dd2b8bd5bdf1989895beb8d39f88a2f595895b66edf7aad20ffbd6cf2e`

```dockerfile
```

-	Layers:
	-	`sha256:8bd1303d556029148a7040fb1ec53ec847e4cb6d399044f8f4b7e982cf607135`  
		Last Modified: Fri, 16 Jan 2026 21:58:30 GMT  
		Size: 5.6 MB (5586355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d098d8ceb9e37f70da4e29e97439abe0305c8aadae217d3666565b2e120f8e14`  
		Last Modified: Fri, 16 Jan 2026 22:45:59 GMT  
		Size: 26.3 KB (26346 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:latest`

```console
$ docker pull ghost@sha256:86090f3ee57af8d8e3fa11875b5787068a1c17b8aebd4b88d932efe11097f578
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
$ docker pull ghost@sha256:ef3782910d75e1a4d0f2fee23d521f47ff4f2dd770a00d6cb4bd5a45c260165d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229949562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e67eca0fbe174babbedbd2b2dab2f54beefaf217dfe3b076edb2941c72d4181`
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
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:50:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:50:51 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:50:51 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:01 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:01 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:52:59 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:00 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:00 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:00 GMT
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
		Last Modified: Wed, 14 Jan 2026 17:59:37 GMT  
		Size: 49.5 MB (49472719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ac2b87b09265a60e104e3d87872d2c15f913cbbfd4d401b5e4b5353e4ced4`  
		Last Modified: Wed, 14 Jan 2026 17:59:48 GMT  
		Size: 1.7 MB (1712660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cc9ecead9d0fe8970f3923a484fcd4fe1fd027fab911d462ca552cd57d5dbf`  
		Last Modified: Wed, 14 Jan 2026 17:59:36 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d9069be84eda409daf000052287ded0488fa41932b208a91d7b5d9c61fb1db`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 1.2 MB (1247544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139dd34f662903c210b176797936f46c21e51067027a573dba8cf698eec3198`  
		Last Modified: Fri, 16 Jan 2026 21:53:42 GMT  
		Size: 11.7 MB (11704039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe03f721169025219aa078337a2541219c5ac7246fb867e8aff113d1e20b884`  
		Last Modified: Fri, 16 Jan 2026 21:53:36 GMT  
		Size: 137.6 MB (137579701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54048a9e0fb4911913295adb6af4358c80b7065fbed3847c9f8896df95c8853`  
		Last Modified: Fri, 16 Jan 2026 21:53:41 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:f0a051f5af0b039dad919753c3041d11088d11264a2d6b34202496fa65ceea68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5618877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aec6fe309a03ace913e95d0b5789af60ff41dc0a6518a6701233a74996e75f8`

```dockerfile
```

-	Layers:
	-	`sha256:939d78f65f1ccf8a812605765fcd939e938d2218ee6f2c787e8b9806c9a9c969`  
		Last Modified: Fri, 16 Jan 2026 22:45:38 GMT  
		Size: 5.6 MB (5592530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa662e79d45a5b6a60edcb33a6f22188c2cfa985ed1b67ef7d9bfef7ebb21087`  
		Last Modified: Fri, 16 Jan 2026 22:45:39 GMT  
		Size: 26.3 KB (26347 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:e710e94955768bd41a14f809d4d928e15a84d8a6245cc224dc99cf2ee2338d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221405328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ddf88f39a855f8364b0c92d1913a540fc11ec7b886d770172e17cab3fbf16a`
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
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:49:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:49:57 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:49:57 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:50:11 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:50:11 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:53:01 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:53:01 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:53:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:01 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:53:01 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
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
	-	`sha256:a249d6508920eeaed8c936fcd9d1266903a78701d8d719939629aecacd2b3612`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 1.2 MB (1214444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cecadaf268b53180de45b75d528261de3e54e528974811d9678e3ad073280`  
		Last Modified: Fri, 16 Jan 2026 21:53:48 GMT  
		Size: 11.7 MB (11694733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df3a8008132b7222b86b8fcf41e409341df064efb15cd0b2db76a2e43652440`  
		Last Modified: Fri, 16 Jan 2026 21:55:08 GMT  
		Size: 138.6 MB (138635032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a54b4827a3677d869daa769f728f3d85ed1c41810346c406ebdba1c9d6017bb`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:bbd9199cb4a5da33fb05a2c105163173092e1633d862b6c8b4709cf5dc9283e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5621812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b6b5679fb62f0751fd471ebda0daf079057a1d2440fb4f139bd37db503a5cb`

```dockerfile
```

-	Layers:
	-	`sha256:ecc780399baa396908b03e0e41b891f1866a69664c910d13f5c8f6839801370a`  
		Last Modified: Fri, 16 Jan 2026 21:53:38 GMT  
		Size: 5.6 MB (5595327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b857b5e875c2615f4e29809571a4619dc21beb25493216bedf4002027ac0ab97`  
		Last Modified: Fri, 16 Jan 2026 22:45:45 GMT  
		Size: 26.5 KB (26485 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:cd23414049a2774d17ae2dd1e327e1037e2ae277751e37e06a25cd0da6a35a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230013156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1383692cd7c356a7a82172e9a8f64527070c1550ab468edb794c3ecc7e285d09`
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
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GOSU_VERSION=1.19
# Fri, 16 Jan 2026 21:51:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 16 Jan 2026 21:51:29 GMT
ENV NODE_ENV=production
# Fri, 16 Jan 2026 21:51:29 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Fri, 16 Jan 2026 21:51:40 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 16 Jan 2026 21:51:40 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:54:06 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:54:06 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:54:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:54:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:54:06 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:54:06 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87c15c864725a8daa5ca1505d5d886e53928b49fa578e7a35dc51a4be5b715d`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4c74fb4662b26fe96702c59c427e26bd0489a0a1c1c5960592b029426583e3`  
		Last Modified: Wed, 14 Jan 2026 18:01:50 GMT  
		Size: 49.6 MB (49611029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20454c8e368d7849b8d2669b17f01d47585f0d71a5b683c0c03997c8733f81d2`  
		Last Modified: Wed, 14 Jan 2026 18:01:55 GMT  
		Size: 1.7 MB (1712623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6686bd0124e3e3612ac03ec0e58e60f1d86a689763f36ecade62f90a4f8d1ea`  
		Last Modified: Wed, 14 Jan 2026 18:01:49 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7033eb962607a955c6372a69ee5257aa923a8d39d76674bd162f2787d935f3a`  
		Last Modified: Fri, 16 Jan 2026 21:54:44 GMT  
		Size: 1.2 MB (1201530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7651bda82d46538be346d839ca10addf26d82eede645b669e55ce70b5f63385`  
		Last Modified: Fri, 16 Jan 2026 21:54:54 GMT  
		Size: 11.7 MB (11703412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc9b9f0753a93ea6ffa5029194830560b1d152496a86a2b86054592ebe5a0c3`  
		Last Modified: Fri, 16 Jan 2026 21:54:47 GMT  
		Size: 137.7 MB (137672344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd6c458dda55df446dcb602d8173c61779b73d3a0ccbf96b3ec524e423e9d3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:53 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:02e7bd8415afbd519cd16da0a7c5f58bed487547a747c2962e0a62f6fd97b13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5619410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834af9f6d47a9d1a26e9c3b13c3ff24c2bf447846c1f4deb20f4a369ccbaae4f`

```dockerfile
```

-	Layers:
	-	`sha256:0ddf820b5a6704d55ee73e6166e8dc592df42b3892756b31e43cd02d23d23cb8`  
		Last Modified: Fri, 16 Jan 2026 22:45:51 GMT  
		Size: 5.6 MB (5592881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05df5e3594cece8c76e3b739c4668dc514e605246c00962e575600b709e88a3e`  
		Last Modified: Fri, 16 Jan 2026 21:54:43 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:c3436627928b1b43d1456845ecbf82ba8d9e3a7e42f317f4a2a18b6a0f4dacfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231935344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43437d8327a686e5f5a504963fdc52b1d29e8051166b368362edf196278c856`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:15:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV NODE_VERSION=22.22.0
# Wed, 14 Jan 2026 21:22:26 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:22:26 GMT
ENV YARN_VERSION=1.22.22
# Wed, 14 Jan 2026 21:23:43 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 21:23:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 21:23:44 GMT
CMD ["node"]
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 22:23:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 22:23:31 GMT
ENV NODE_ENV=production
# Thu, 15 Jan 2026 22:23:31 GMT
ENV GHOST_CLI_VERSION=1.28.4
# Thu, 15 Jan 2026 22:23:54 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 15 Jan 2026 22:23:54 GMT
ENV GHOST_VERSION=6.13.2
# Fri, 16 Jan 2026 21:57:35 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends g++ make python3; 		gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8*; 		cd current; 	gosu node node -e 'require("sqlite3"); require("sharp");' # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
WORKDIR /var/lib/ghost
# Fri, 16 Jan 2026 21:57:35 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 16 Jan 2026 21:57:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:57:35 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 16 Jan 2026 21:57:35 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d139ad9a3a58767f140c3201036e062e1a612d605a2d9ad8f971d9d78b53105`  
		Last Modified: Tue, 13 Jan 2026 02:16:16 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b8ffadc3140bf38490474eefe010b5d358986aad8d44529804b0743054faac`  
		Last Modified: Wed, 14 Jan 2026 21:24:32 GMT  
		Size: 49.7 MB (49677854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d962a7944bc35ac4232287b29129631cb30e0c2303fe9accd5060e13d10e417c`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 1.7 MB (1713059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b2eef94eee0b83f1a3d7a9599195e40b2dc80c3676e1214811bd87d43ba5c6`  
		Last Modified: Wed, 14 Jan 2026 21:24:28 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9743a6eb0019afb918d9a783e9824fd189d217337fdd105c51b13324597390`  
		Last Modified: Thu, 15 Jan 2026 23:29:01 GMT  
		Size: 1.2 MB (1221797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dc1783fd9f5092bf435b4a7176f1ffa2e2a22e9cb73e36790448ef519cc84d`  
		Last Modified: Thu, 15 Jan 2026 22:27:23 GMT  
		Size: 11.7 MB (11713708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad56df80bd6319c74dfc884bd19c872678904e3b83a9172205691d51dccf11b`  
		Last Modified: Fri, 16 Jan 2026 21:58:54 GMT  
		Size: 140.7 MB (140720181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d310d3c0fa29617bb1c71502f8aa26ec106e911099b6ead0f3fe978b9fe79f3`  
		Last Modified: Fri, 16 Jan 2026 21:58:39 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:77c6a5256641362cf56117a966d9303ba1632d8372901ae78527d59d41ecb9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4c08dd2b8bd5bdf1989895beb8d39f88a2f595895b66edf7aad20ffbd6cf2e`

```dockerfile
```

-	Layers:
	-	`sha256:8bd1303d556029148a7040fb1ec53ec847e4cb6d399044f8f4b7e982cf607135`  
		Last Modified: Fri, 16 Jan 2026 21:58:30 GMT  
		Size: 5.6 MB (5586355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d098d8ceb9e37f70da4e29e97439abe0305c8aadae217d3666565b2e120f8e14`  
		Last Modified: Fri, 16 Jan 2026 22:45:59 GMT  
		Size: 26.3 KB (26346 bytes)  
		MIME: application/vnd.in-toto+json

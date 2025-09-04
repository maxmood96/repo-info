<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:5`](#ghost5)
-	[`ghost:5-alpine`](#ghost5-alpine)
-	[`ghost:5.130`](#ghost5130)
-	[`ghost:5.130-alpine`](#ghost5130-alpine)
-	[`ghost:5.130.4`](#ghost51304)
-	[`ghost:5.130.4-alpine`](#ghost51304-alpine)
-	[`ghost:6`](#ghost6)
-	[`ghost:6-alpine`](#ghost6-alpine)
-	[`ghost:6.0`](#ghost60)
-	[`ghost:6.0-alpine`](#ghost60-alpine)
-	[`ghost:6.0.6`](#ghost606)
-	[`ghost:6.0.6-alpine`](#ghost606-alpine)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:latest`](#ghostlatest)

## `ghost:5`

```console
$ docker pull ghost@sha256:13af85b409bddc414418ed1aefea4339ef11d70b79daaa70cfd8d5ddfed3bde2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:5` - linux; amd64

```console
$ docker pull ghost@sha256:b708658fb27413945daa9986cf8566160728af899ddf7c449c53a5af5d8a2648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192522180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311211c3d264cee8cda0d7a5fd42bee340a61435ef298ac295bcd1ae03678e79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 13 Aug 2025 02:19:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4733cb89761b11d3b538fd74d6219198e0dd771200912407122d14b2670815`  
		Last Modified: Wed, 03 Sep 2025 21:07:39 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da230fee1a10de928e261cc92d3372d190cd29ea0e6f71177a6987a382b87e4`  
		Last Modified: Wed, 03 Sep 2025 21:07:41 GMT  
		Size: 41.0 MB (40977768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf37311b43e9505cacdcd82aa37169cc3f42aacb75a163605e9092ba8bdf11d`  
		Last Modified: Wed, 03 Sep 2025 21:07:39 GMT  
		Size: 1.7 MB (1712561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d3f25a0e331e1f50f1b678c3a29ae5279356d8999e87b4d7d8e95aaa11c9d3`  
		Last Modified: Wed, 03 Sep 2025 21:07:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cffbf174346f17c550affa3240baf4f0197bb0584b5e2076026c9229b5a2b29`  
		Last Modified: Wed, 03 Sep 2025 21:10:12 GMT  
		Size: 1.4 MB (1444930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099260993daa4dd7302111064c0de72604fca27ee27010a390a6ad084dbc78f2`  
		Last Modified: Wed, 03 Sep 2025 21:10:14 GMT  
		Size: 11.1 MB (11071502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3d719ab3e4524b94610a70a2718437cc14d2b80e4d94163c22060864f40f69`  
		Last Modified: Wed, 03 Sep 2025 21:10:28 GMT  
		Size: 109.1 MB (109080828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e128a7c9170bcca829336cf757a1d74c66b79af3b1530a151b15e4b839a3b5`  
		Last Modified: Wed, 03 Sep 2025 21:10:13 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:b0f2dfb0b5ba70239b1b38c7c5369b4b57ece9414ad04a4e96912af9120b5c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6750e7db3f4f9aa29a29194a9c75007212824f1568a8b9b8cc69dd7043f071fa`

```dockerfile
```

-	Layers:
	-	`sha256:081f84e98559d922114e02ecf535d591da789e0b7143ae439100d1c5db66c9d6`  
		Last Modified: Thu, 04 Sep 2025 00:45:32 GMT  
		Size: 5.5 MB (5538655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c21ce37cd62b0c0508f834423979ee495d99d198be06e86ae8e83d22977c163`  
		Last Modified: Thu, 04 Sep 2025 00:45:33 GMT  
		Size: 29.0 KB (29014 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm variant v7

```console
$ docker pull ghost@sha256:3c6241cd855b10132734a41e49c6f91f5a03b4d037f1855dec023b0b04cbd49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195794297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37188079b442f39faf8a080eb082291f4f6329525b8f000f10b24a791f48fc3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 13 Aug 2025 02:19:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae1e510a43ef8f416095b11f0182b2e280a16abb567ffe9973ee818f1ced070`  
		Last Modified: Wed, 13 Aug 2025 00:43:01 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4bcd4f3d11b003db3518f4a0713f95cc798b21c548a3ccd283119d9444fe49`  
		Last Modified: Wed, 03 Sep 2025 22:14:13 GMT  
		Size: 37.1 MB (37064132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fc96186c22f4a3af271347e6c955d9498ea60891c5d38188dac326ee76c7d0`  
		Last Modified: Wed, 03 Sep 2025 22:14:05 GMT  
		Size: 1.7 MB (1712733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c993896595cfc57bb020e68783a9a2081ea6e5c5d4580a8cbaf6a2f395acc903`  
		Last Modified: Wed, 03 Sep 2025 22:14:04 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e408b2e58ff20b50d8d71dfb4c8f2129b89ddb236d51e9299bc46185934c8f3`  
		Last Modified: Wed, 03 Sep 2025 23:16:09 GMT  
		Size: 1.4 MB (1412584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346c9c473548776cd17836990f8faae75f71272a59a19233b76019268ddbbe22`  
		Last Modified: Wed, 03 Sep 2025 23:16:11 GMT  
		Size: 11.1 MB (11071877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8c8a7bf8dcad2a81142b0cc770783f8379e3a4d32a33476c1395c193e1183a`  
		Last Modified: Wed, 03 Sep 2025 23:16:27 GMT  
		Size: 120.6 MB (120589709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef19e20e6c283d2aea4572b2e99069d772a7186734116df72d083c53e397d560`  
		Last Modified: Wed, 03 Sep 2025 23:16:09 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:f7ed0fc59cb0df448a75ef934c18d9e25909f88361afd976396cd683979c9ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5570518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df583ee60a866f3fd11f1ef29901f2243172279f666956c97c4d4305cf9be344`

```dockerfile
```

-	Layers:
	-	`sha256:810f1412a453a102f19703c7dc1bbc386910c7a84edcb0abf5247d4b3f249046`  
		Last Modified: Thu, 04 Sep 2025 00:45:39 GMT  
		Size: 5.5 MB (5541410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3349d4ae03f9717f2633f767770ea5ca5b2668104538fa49692f2c08682a34b`  
		Last Modified: Thu, 04 Sep 2025 00:45:40 GMT  
		Size: 29.1 KB (29108 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:a91eb3665ee3884b833b83e6cf8b191ab575481f77744638424f53aace422170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192375878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03aeb5fd265f63a7b8ec1a4cfb86aa20ac7660fdb131493a799549cb3345b7c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 13 Aug 2025 02:19:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27263372d67228bb86c6e522c8fc32c5e6a4a10ddabec215fa8026f3d01a3508`  
		Last Modified: Thu, 28 Aug 2025 14:40:51 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2518670ec6f69a0f47a52c0f889152d9f59f5696aea4f65c7738975a3ff4fac6`  
		Last Modified: Wed, 03 Sep 2025 21:23:49 GMT  
		Size: 40.9 MB (40939649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bded516fefd7eab843a38696ab759387eea7ef0a141a2f721999709cfd27e53f`  
		Last Modified: Wed, 03 Sep 2025 21:23:45 GMT  
		Size: 1.7 MB (1712624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c59bbf66433150dcfe0f4cff482e662861d1b5087f97754c55c1dccd1c233f4`  
		Last Modified: Wed, 03 Sep 2025 21:23:45 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eefb2b1951c8ff402843632e7f613eed2998393b4737a4a078aea9be891a32e`  
		Last Modified: Wed, 03 Sep 2025 22:12:58 GMT  
		Size: 1.4 MB (1376742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2255fdd165f93bc1f5313ac8023807e7d638bc3655afa084bff339792392a5`  
		Last Modified: Wed, 03 Sep 2025 22:13:01 GMT  
		Size: 11.1 MB (11071993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4190b44a91f23582dd26283fbe5168cad1d34efb257b71d338f84fc10e7249`  
		Last Modified: Wed, 03 Sep 2025 22:13:06 GMT  
		Size: 109.2 MB (109188537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61dcdf8f271e5a205e84daaa269033d79d461e7f09835b556b67bb2bbaefe85c`  
		Last Modified: Wed, 03 Sep 2025 22:13:00 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:f531c8a9df549c87b2243de5b8e58d1c47b9012ee0d164982b814a287fcf3b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c821b8e1d532126f3afcf67891ea7dc3b6faabadba0543cb8e5338658a3186e`

```dockerfile
```

-	Layers:
	-	`sha256:186f5ea75fc4e6968575aed2e85344bf7326652cf9d2ee16f6aab9bab7d9e48f`  
		Last Modified: Thu, 04 Sep 2025 00:45:45 GMT  
		Size: 5.5 MB (5538946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9c8867ad1537600d462622e255fabed6eb6c00a639fb44f0131731a576ce87`  
		Last Modified: Thu, 04 Sep 2025 00:45:46 GMT  
		Size: 29.1 KB (29136 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; ppc64le

```console
$ docker pull ghost@sha256:5eef4c5fe4b005f7fbbbd12af9ecb44d636a9b72e22224e377cde56547a295d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.2 MB (213213895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407c5f3d8a8cbfeefb5113c4f4ea32a13dabbc03cb16d7a54711da80d616b289`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 13 Aug 2025 02:19:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db49890cc93d9412b095c6d9e7c7dcd1224e0b5c93c9c8848c12d48ecffbb89a`  
		Last Modified: Wed, 13 Aug 2025 13:16:33 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82069806ce067cfe764da9862c1d3880e4de07fe659a1dcc35e05a5f703b380c`  
		Last Modified: Wed, 03 Sep 2025 23:07:26 GMT  
		Size: 43.5 MB (43469521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dcae3e4550644ec520c3da3c7a5351ffef1ea4e938911c0bc6883e648dc493`  
		Last Modified: Wed, 03 Sep 2025 21:58:55 GMT  
		Size: 1.7 MB (1712746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f616b2d0e663d180ffc95a63e2a12c2bb578e3ef724f5357d6459c02c587bfb`  
		Last Modified: Wed, 03 Sep 2025 21:58:56 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48f0afd3003f91fda85b8fa35aa74ef1071291c271c7d295a0b381d437e25a6`  
		Last Modified: Wed, 03 Sep 2025 22:21:06 GMT  
		Size: 1.4 MB (1366801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab475f2027f5e7e7387b4cadf343389a0494b8ce0a437a02f629fef42f3951b5`  
		Last Modified: Wed, 03 Sep 2025 22:21:08 GMT  
		Size: 11.1 MB (11071290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c00f4dc7cfca47161dc50f5e811aa0b1b5a24604f2e458e3637c7bcce0dbc0e`  
		Last Modified: Wed, 03 Sep 2025 22:21:20 GMT  
		Size: 123.5 MB (123515780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc301d8e0285057786e500c0dd71d20c458646631597b52bd6a200df5690504c`  
		Last Modified: Wed, 03 Sep 2025 22:21:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:5628823fd20dfac1fe25ac5bf5e52b514139c5b17c29f5d2b11422105bf6616b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8f0ba92a5bd237e399433f3181b6d1ddbbdfab8a485d4a02639cb9a4ee601d`

```dockerfile
```

-	Layers:
	-	`sha256:c2834bb66618172f229e2ab92f8944468c3565a30ca12170c67f6d2cf69edc0b`  
		Last Modified: Thu, 04 Sep 2025 00:45:51 GMT  
		Size: 5.5 MB (5538500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5996fd8bb0600585c1089f8c81d3d8669e19b575e61e7fd5068bbeb6c55e6370`  
		Last Modified: Thu, 04 Sep 2025 00:45:51 GMT  
		Size: 29.1 KB (29055 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5` - linux; s390x

```console
$ docker pull ghost@sha256:01a31d1ac0f77574956342cb049e74b910d8816010d659f6bb78bc6092f4f325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204963295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2c96b382e65462523b7e154bdce6c50dba0981548c3eeffeb1627f8709c530`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 13 Aug 2025 02:19:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dadfc3ada3cd4f49e71dc39867db6cf8d4c2cb806f817ea84710057fd1995b`  
		Last Modified: Wed, 13 Aug 2025 15:28:53 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cf7bcb01d49fe8baaafab6d3baac3b451acab827c4ad06b02e9d3ae34486bd`  
		Last Modified: Wed, 03 Sep 2025 22:06:16 GMT  
		Size: 41.2 MB (41222537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89207a8592308cc545b6f73e5a3c4b6aa3204af29454a72ce9f19bf9df3ba5a1`  
		Last Modified: Wed, 03 Sep 2025 22:06:14 GMT  
		Size: 1.7 MB (1712554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac75b645d2254afb8a4f6736b609714f769375ae1e31bf9d2499cf6023437b17`  
		Last Modified: Wed, 03 Sep 2025 22:06:14 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c84a8ea6c419a5caad58c4a291506de73829b25915d2bebc5a61a6c161434d`  
		Last Modified: Wed, 03 Sep 2025 22:18:51 GMT  
		Size: 1.4 MB (1410230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee2e3a4f2ccfcbb5166e0952374fcc01b7420e3d1fda8293bc33805424deec1`  
		Last Modified: Wed, 03 Sep 2025 22:18:52 GMT  
		Size: 11.1 MB (11071555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13de54eaa4dae667fc0e76b0dd29b72ceff3e31a12dcfd009f0c69fd459b0b4`  
		Last Modified: Wed, 03 Sep 2025 22:19:00 GMT  
		Size: 122.7 MB (122654261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d998a9c8c5247811966fbb13d5e0faea9447fa214df71570c6c262a0ef3ac43a`  
		Last Modified: Wed, 03 Sep 2025 22:18:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5` - unknown; unknown

```console
$ docker pull ghost@sha256:945143e3f85e3d08b620946893f48235d4405b1e0ff8a827a379b40b09de105d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67138c2398e29bed49646c1f27a1eb1c889df60026e213e5df07e73a25016e0`

```dockerfile
```

-	Layers:
	-	`sha256:6a5c44e5d19caa1efa403ff4c6a8a68cb350bfc3bed36a3656d3ecee994840ad`  
		Last Modified: Thu, 04 Sep 2025 00:45:56 GMT  
		Size: 5.5 MB (5532478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba483f5452f593bb948fbf74c1106fe761e2c505fbe45c86c501f3d187d4780`  
		Last Modified: Thu, 04 Sep 2025 00:45:57 GMT  
		Size: 29.0 KB (29013 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5-alpine`

```console
$ docker pull ghost@sha256:cac8c28d63e68edcfd80389c97fc256da20d897e3d0901ec6b05618e54800e64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:d5cb0f8f3cd02fbb62bdc4b981bcda5c4e7206947353aca440e42bd80e14176b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166807509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d63f9cdba50d85f6e1ba2a8ee7be2beb4910cbea7795fea16de2a99f9039cd7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88300f8759af46375ccc157a0a0dbf7cdaeded52394b5ce2ce074e3b773fe82`  
		Last Modified: Wed, 03 Sep 2025 20:29:11 GMT  
		Size: 42.8 MB (42750733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd345d7e43c58474c833bee593321ab1097dd720bebd8032e75fbf5b81b1e554`  
		Last Modified: Wed, 03 Sep 2025 20:29:08 GMT  
		Size: 1.3 MB (1260576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de821d16564893ff12fae9499550711d92157ed1e6705a8c7f7e63eac0a2bb9`  
		Last Modified: Wed, 03 Sep 2025 20:29:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089ecb353a985c02c4a60ed3b041ab383897fb1212e1e951bb2a8583e41267ff`  
		Last Modified: Wed, 03 Sep 2025 21:10:13 GMT  
		Size: 777.0 KB (777041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35313b08dcca3c86127d0c0678c3ae54dd558ec22f1d6e1343e305ee0c70e7ca`  
		Last Modified: Wed, 03 Sep 2025 21:10:13 GMT  
		Size: 1.1 MB (1119667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7bd0e2cf124c7cee51b79233f00ad9e2f6e33a1e0544d0c110a8453f5da3d2`  
		Last Modified: Wed, 03 Sep 2025 21:10:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f0a4ecf244cac89f2fa466907d39436d5d662f7b08b134afbd5979da9a079a`  
		Last Modified: Wed, 03 Sep 2025 21:10:15 GMT  
		Size: 11.1 MB (11072137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f2ff5a9280ad28a3d710c276bbe41118b4e2e68cb842697713da95cc20d0ff`  
		Last Modified: Wed, 03 Sep 2025 21:10:34 GMT  
		Size: 106.0 MB (106026471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29306af234df90804ed2099ce58608a6bccf8080f4e6a6c02cd565b8f9225aad`  
		Last Modified: Wed, 03 Sep 2025 21:10:15 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:bfc4cc04127df728a9f1562c7c9813af6b5cb8b190d7accff3b68204fdb8d60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fc59a7dcfa9d13a70c596dc3c5f94d22333aaa5e3f0ff7b13abda182bbfc93`

```dockerfile
```

-	Layers:
	-	`sha256:ba0df3526181df2df82c1e7eff6ae08dd49fe5bf894a45ec15d05c887165da9c`  
		Last Modified: Thu, 04 Sep 2025 00:45:49 GMT  
		Size: 3.3 MB (3327656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ede73372ba139363feb614fba3ff6becb8c77d15039798d9c520bca242986aef`  
		Last Modified: Thu, 04 Sep 2025 00:45:50 GMT  
		Size: 32.0 KB (31987 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:eb608fa4cda5d74361522caa0401b8c5bd901b5808a7d049b696163e057d82ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179432613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f107b730fbb85bc5f80d625c10bbc5dc3b31e0c7e46823bcab3d669ec4481f41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c533aeba408974e594ea5abca2331989c4f9224b40535f05cb74268ac2ee5bd2`  
		Last Modified: Wed, 03 Sep 2025 22:10:49 GMT  
		Size: 41.0 MB (41036904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bef4fd64b731a7dbaa685234c290f08ea5fb12da71db7f2c3cc63c5cea422b`  
		Last Modified: Wed, 03 Sep 2025 22:10:44 GMT  
		Size: 1.3 MB (1260557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd71b6fecbcefd165694195568ae1093f182b78f1e5400e966ebce9e19df23b`  
		Last Modified: Wed, 03 Sep 2025 22:10:44 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9568b30b545fbb29f4e949ac3df28c4d652eb2c8423f3818b7d68adc28c73485`  
		Last Modified: Wed, 03 Sep 2025 23:17:44 GMT  
		Size: 766.1 KB (766086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a3a09e68a81b9a49664458407175080bd86669aa7e1ddbb79c86a9edef5f8e`  
		Last Modified: Wed, 03 Sep 2025 23:17:44 GMT  
		Size: 1.1 MB (1086411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2087e84578591d1182129c1935e1e80d59544000e520cad85100654e531b87e7`  
		Last Modified: Wed, 03 Sep 2025 23:17:45 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64996ebfc19e794d4de26f10611c5dc41e98c0b2470e602b28a1422d333fce23`  
		Last Modified: Wed, 03 Sep 2025 23:17:46 GMT  
		Size: 11.1 MB (11082699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d7126551ddbccc7aee0df08f2ca21a2407f38ca2895a37d5e0a526c257d585`  
		Last Modified: Wed, 03 Sep 2025 23:17:56 GMT  
		Size: 120.7 MB (120697857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff05f03661b17772c3de3233f5ddcd5b108277eb52319a4ba577e00eab40f23a`  
		Last Modified: Wed, 03 Sep 2025 23:17:45 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:7ea2fd9bd3623fa274acb0e4e31fbd8450785b8e08bd4758421daeb2309b885f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd70712c1d84e9a9e9797ea74eecfcd64c054d7103ac3867b65178270e94ce7d`

```dockerfile
```

-	Layers:
	-	`sha256:b1ce8690c10988ee5220caa608171cb2b9800f1023a3ad555fed93708ea8a30a`  
		Last Modified: Thu, 04 Sep 2025 00:45:54 GMT  
		Size: 31.9 KB (31893 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:bbf54f2a88185368d6fe7a7077889a80b6065388e5438e6fdc7e8e8795a9ecad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 MB (178243186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79413a928959c779c960d662180b5624f36cccaaa14745868b26e541644b2089`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb4140b5e03430fe1f2e569e8dc5530627a98d42bc658ef64673aa619e6f27`  
		Last Modified: Wed, 03 Sep 2025 22:11:44 GMT  
		Size: 40.5 MB (40493858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddfda3d4b1769d00c0ce7b336b8c0013e9478a7849f8e683a838fd8028725c9`  
		Last Modified: Wed, 03 Sep 2025 22:11:42 GMT  
		Size: 1.3 MB (1260551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43288fb01db5bf2af65a1de4e1bea8a08196ea5a31d3085a15aac9fde3c93c15`  
		Last Modified: Wed, 03 Sep 2025 22:11:41 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce0b0631776b8d519e672b262851fddb80995f34c40bdf40867d3f63104ec73`  
		Last Modified: Wed, 03 Sep 2025 23:22:54 GMT  
		Size: 701.5 KB (701475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e390b9e175abedc487f7869760481fe395f2cc0b37fc4370717e8ce583d9c9`  
		Last Modified: Wed, 03 Sep 2025 23:22:54 GMT  
		Size: 1.1 MB (1086407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e0dbc2769f9074ade9083fba7b88217de9fb05be2140b24f4da459622ea3ff`  
		Last Modified: Wed, 03 Sep 2025 23:22:54 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4d28d97547cd4de17234ede1aa07b4f4a56c3a5fcb0d5e895b9d27c40307`  
		Last Modified: Wed, 03 Sep 2025 23:22:57 GMT  
		Size: 11.1 MB (11071916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43f0c035cc1987950b4c72bab9c8e8c64badb4056ae9437a10debc97edb99fd`  
		Last Modified: Wed, 03 Sep 2025 23:23:03 GMT  
		Size: 120.4 MB (120408752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872fedc0aca5a893792a516ace674d63d54e472ce23f5a9802499d62dabe450a`  
		Last Modified: Wed, 03 Sep 2025 23:22:56 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:dcc187cc6bba04ede3816939db84a0595a822a08dafff3dfada952b5f5253ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3356777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04351db5cb4c7abcaef6c0716b47986c5e829791e0525b9631f64beec54f8b7c`

```dockerfile
```

-	Layers:
	-	`sha256:e74f62c324b176ee0cc3e1ad57c06ce75bb8c79e57e088c1926a7803136d677b`  
		Last Modified: Thu, 04 Sep 2025 00:45:58 GMT  
		Size: 3.3 MB (3324669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:091a419f9643fda9b99bdb6d8f0870dee80ba13da022784ee9af36094a6a4714`  
		Last Modified: Thu, 04 Sep 2025 00:45:59 GMT  
		Size: 32.1 KB (32108 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:3cec8973df5e31133d48aca400a8e43d5e1ce88c9528afe97b906e67e95395ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186298708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1daa1350bc99bd62f406f70768fe4297637b70e22803c42846e187098305d65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8e8228254a218fbf68fbf8d7093ea99dfce63dd0a72ad0cc8be65e6da3f7c8`  
		Last Modified: Wed, 03 Sep 2025 21:21:49 GMT  
		Size: 42.4 MB (42433073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c149c7c96aa9b49de8c5de3415d3692e81ced50773077ea0be1a0f3f36032234`  
		Last Modified: Wed, 03 Sep 2025 21:21:43 GMT  
		Size: 1.3 MB (1260573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127c05f5df6b075d5c314444a05d3de523268e2de5e9b235e7ba72aa60ed3c61`  
		Last Modified: Wed, 03 Sep 2025 21:21:43 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21a07352734c4f136c142d20b2cf994e5c6256385e224650deceb893f8d1b33`  
		Last Modified: Wed, 03 Sep 2025 22:17:00 GMT  
		Size: 838.6 KB (838576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28887b48c1997751c390dfc44704bda2dfe64d584b7b896595205e775066555c`  
		Last Modified: Wed, 03 Sep 2025 22:17:00 GMT  
		Size: 1.0 MB (1046721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5038a642123ae385b43d639ceb0b1d84fbae53e1c8aaebca3e0c5c9975da26`  
		Last Modified: Wed, 03 Sep 2025 22:17:00 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc4259dbd9c5928cef457319ce2222df4d97405cfebce48325f9038f8c6eaa0`  
		Last Modified: Wed, 03 Sep 2025 22:17:01 GMT  
		Size: 11.1 MB (11071509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55c51524d86fda2d1932ac29d7009e00aeb4e55f03aeb9fa55b66d11a8db22a`  
		Last Modified: Wed, 03 Sep 2025 22:17:23 GMT  
		Size: 125.5 MB (125516320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7417398f7cf371a2155a9c915c915945a4003ed24b0fd70648677673f048fec0`  
		Last Modified: Wed, 03 Sep 2025 22:17:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:b0f4847bc476a97f5630ffe64aff4d265cf6c02f71036715479c30b58437d35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3193e302105b224bd96838e7c3371ebf087b18a4f4821d7a8509607930e0dce8`

```dockerfile
```

-	Layers:
	-	`sha256:5f81bf1bb62eac5fe1d84c2a4e23c6f6a82791b8690b90b8ea07f226b0fc4e2b`  
		Last Modified: Thu, 04 Sep 2025 00:46:03 GMT  
		Size: 3.3 MB (3327752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32488d9cc32fbc2d3e91e5fd8e0b48d27364010639a77bc88d90cbbadcc6fa25`  
		Last Modified: Thu, 04 Sep 2025 00:46:04 GMT  
		Size: 32.1 KB (32140 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130`

```console
$ docker pull ghost@sha256:13af85b409bddc414418ed1aefea4339ef11d70b79daaa70cfd8d5ddfed3bde2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:5.130` - linux; amd64

```console
$ docker pull ghost@sha256:b708658fb27413945daa9986cf8566160728af899ddf7c449c53a5af5d8a2648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192522180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311211c3d264cee8cda0d7a5fd42bee340a61435ef298ac295bcd1ae03678e79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 13 Aug 2025 02:19:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4733cb89761b11d3b538fd74d6219198e0dd771200912407122d14b2670815`  
		Last Modified: Wed, 03 Sep 2025 21:07:39 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da230fee1a10de928e261cc92d3372d190cd29ea0e6f71177a6987a382b87e4`  
		Last Modified: Wed, 03 Sep 2025 21:07:41 GMT  
		Size: 41.0 MB (40977768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf37311b43e9505cacdcd82aa37169cc3f42aacb75a163605e9092ba8bdf11d`  
		Last Modified: Wed, 03 Sep 2025 21:07:39 GMT  
		Size: 1.7 MB (1712561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d3f25a0e331e1f50f1b678c3a29ae5279356d8999e87b4d7d8e95aaa11c9d3`  
		Last Modified: Wed, 03 Sep 2025 21:07:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cffbf174346f17c550affa3240baf4f0197bb0584b5e2076026c9229b5a2b29`  
		Last Modified: Wed, 03 Sep 2025 21:10:12 GMT  
		Size: 1.4 MB (1444930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099260993daa4dd7302111064c0de72604fca27ee27010a390a6ad084dbc78f2`  
		Last Modified: Wed, 03 Sep 2025 21:10:14 GMT  
		Size: 11.1 MB (11071502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3d719ab3e4524b94610a70a2718437cc14d2b80e4d94163c22060864f40f69`  
		Last Modified: Wed, 03 Sep 2025 21:10:28 GMT  
		Size: 109.1 MB (109080828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e128a7c9170bcca829336cf757a1d74c66b79af3b1530a151b15e4b839a3b5`  
		Last Modified: Wed, 03 Sep 2025 21:10:13 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:b0f2dfb0b5ba70239b1b38c7c5369b4b57ece9414ad04a4e96912af9120b5c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6750e7db3f4f9aa29a29194a9c75007212824f1568a8b9b8cc69dd7043f071fa`

```dockerfile
```

-	Layers:
	-	`sha256:081f84e98559d922114e02ecf535d591da789e0b7143ae439100d1c5db66c9d6`  
		Last Modified: Thu, 04 Sep 2025 00:45:32 GMT  
		Size: 5.5 MB (5538655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c21ce37cd62b0c0508f834423979ee495d99d198be06e86ae8e83d22977c163`  
		Last Modified: Thu, 04 Sep 2025 00:45:33 GMT  
		Size: 29.0 KB (29014 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; arm variant v7

```console
$ docker pull ghost@sha256:3c6241cd855b10132734a41e49c6f91f5a03b4d037f1855dec023b0b04cbd49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195794297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37188079b442f39faf8a080eb082291f4f6329525b8f000f10b24a791f48fc3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 13 Aug 2025 02:19:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae1e510a43ef8f416095b11f0182b2e280a16abb567ffe9973ee818f1ced070`  
		Last Modified: Wed, 13 Aug 2025 00:43:01 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4bcd4f3d11b003db3518f4a0713f95cc798b21c548a3ccd283119d9444fe49`  
		Last Modified: Wed, 03 Sep 2025 22:14:13 GMT  
		Size: 37.1 MB (37064132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fc96186c22f4a3af271347e6c955d9498ea60891c5d38188dac326ee76c7d0`  
		Last Modified: Wed, 03 Sep 2025 22:14:05 GMT  
		Size: 1.7 MB (1712733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c993896595cfc57bb020e68783a9a2081ea6e5c5d4580a8cbaf6a2f395acc903`  
		Last Modified: Wed, 03 Sep 2025 22:14:04 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e408b2e58ff20b50d8d71dfb4c8f2129b89ddb236d51e9299bc46185934c8f3`  
		Last Modified: Wed, 03 Sep 2025 23:16:09 GMT  
		Size: 1.4 MB (1412584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346c9c473548776cd17836990f8faae75f71272a59a19233b76019268ddbbe22`  
		Last Modified: Wed, 03 Sep 2025 23:16:11 GMT  
		Size: 11.1 MB (11071877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8c8a7bf8dcad2a81142b0cc770783f8379e3a4d32a33476c1395c193e1183a`  
		Last Modified: Wed, 03 Sep 2025 23:16:27 GMT  
		Size: 120.6 MB (120589709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef19e20e6c283d2aea4572b2e99069d772a7186734116df72d083c53e397d560`  
		Last Modified: Wed, 03 Sep 2025 23:16:09 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:f7ed0fc59cb0df448a75ef934c18d9e25909f88361afd976396cd683979c9ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5570518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df583ee60a866f3fd11f1ef29901f2243172279f666956c97c4d4305cf9be344`

```dockerfile
```

-	Layers:
	-	`sha256:810f1412a453a102f19703c7dc1bbc386910c7a84edcb0abf5247d4b3f249046`  
		Last Modified: Thu, 04 Sep 2025 00:45:39 GMT  
		Size: 5.5 MB (5541410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3349d4ae03f9717f2633f767770ea5ca5b2668104538fa49692f2c08682a34b`  
		Last Modified: Thu, 04 Sep 2025 00:45:40 GMT  
		Size: 29.1 KB (29108 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:a91eb3665ee3884b833b83e6cf8b191ab575481f77744638424f53aace422170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192375878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03aeb5fd265f63a7b8ec1a4cfb86aa20ac7660fdb131493a799549cb3345b7c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 13 Aug 2025 02:19:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27263372d67228bb86c6e522c8fc32c5e6a4a10ddabec215fa8026f3d01a3508`  
		Last Modified: Thu, 28 Aug 2025 14:40:51 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2518670ec6f69a0f47a52c0f889152d9f59f5696aea4f65c7738975a3ff4fac6`  
		Last Modified: Wed, 03 Sep 2025 21:23:49 GMT  
		Size: 40.9 MB (40939649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bded516fefd7eab843a38696ab759387eea7ef0a141a2f721999709cfd27e53f`  
		Last Modified: Wed, 03 Sep 2025 21:23:45 GMT  
		Size: 1.7 MB (1712624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c59bbf66433150dcfe0f4cff482e662861d1b5087f97754c55c1dccd1c233f4`  
		Last Modified: Wed, 03 Sep 2025 21:23:45 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eefb2b1951c8ff402843632e7f613eed2998393b4737a4a078aea9be891a32e`  
		Last Modified: Wed, 03 Sep 2025 22:12:58 GMT  
		Size: 1.4 MB (1376742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2255fdd165f93bc1f5313ac8023807e7d638bc3655afa084bff339792392a5`  
		Last Modified: Wed, 03 Sep 2025 22:13:01 GMT  
		Size: 11.1 MB (11071993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4190b44a91f23582dd26283fbe5168cad1d34efb257b71d338f84fc10e7249`  
		Last Modified: Wed, 03 Sep 2025 22:13:06 GMT  
		Size: 109.2 MB (109188537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61dcdf8f271e5a205e84daaa269033d79d461e7f09835b556b67bb2bbaefe85c`  
		Last Modified: Wed, 03 Sep 2025 22:13:00 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:f531c8a9df549c87b2243de5b8e58d1c47b9012ee0d164982b814a287fcf3b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c821b8e1d532126f3afcf67891ea7dc3b6faabadba0543cb8e5338658a3186e`

```dockerfile
```

-	Layers:
	-	`sha256:186f5ea75fc4e6968575aed2e85344bf7326652cf9d2ee16f6aab9bab7d9e48f`  
		Last Modified: Thu, 04 Sep 2025 00:45:45 GMT  
		Size: 5.5 MB (5538946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9c8867ad1537600d462622e255fabed6eb6c00a639fb44f0131731a576ce87`  
		Last Modified: Thu, 04 Sep 2025 00:45:46 GMT  
		Size: 29.1 KB (29136 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; ppc64le

```console
$ docker pull ghost@sha256:5eef4c5fe4b005f7fbbbd12af9ecb44d636a9b72e22224e377cde56547a295d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.2 MB (213213895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407c5f3d8a8cbfeefb5113c4f4ea32a13dabbc03cb16d7a54711da80d616b289`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 13 Aug 2025 02:19:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db49890cc93d9412b095c6d9e7c7dcd1224e0b5c93c9c8848c12d48ecffbb89a`  
		Last Modified: Wed, 13 Aug 2025 13:16:33 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82069806ce067cfe764da9862c1d3880e4de07fe659a1dcc35e05a5f703b380c`  
		Last Modified: Wed, 03 Sep 2025 23:07:26 GMT  
		Size: 43.5 MB (43469521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dcae3e4550644ec520c3da3c7a5351ffef1ea4e938911c0bc6883e648dc493`  
		Last Modified: Wed, 03 Sep 2025 21:58:55 GMT  
		Size: 1.7 MB (1712746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f616b2d0e663d180ffc95a63e2a12c2bb578e3ef724f5357d6459c02c587bfb`  
		Last Modified: Wed, 03 Sep 2025 21:58:56 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48f0afd3003f91fda85b8fa35aa74ef1071291c271c7d295a0b381d437e25a6`  
		Last Modified: Wed, 03 Sep 2025 22:21:06 GMT  
		Size: 1.4 MB (1366801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab475f2027f5e7e7387b4cadf343389a0494b8ce0a437a02f629fef42f3951b5`  
		Last Modified: Wed, 03 Sep 2025 22:21:08 GMT  
		Size: 11.1 MB (11071290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c00f4dc7cfca47161dc50f5e811aa0b1b5a24604f2e458e3637c7bcce0dbc0e`  
		Last Modified: Wed, 03 Sep 2025 22:21:20 GMT  
		Size: 123.5 MB (123515780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc301d8e0285057786e500c0dd71d20c458646631597b52bd6a200df5690504c`  
		Last Modified: Wed, 03 Sep 2025 22:21:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:5628823fd20dfac1fe25ac5bf5e52b514139c5b17c29f5d2b11422105bf6616b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8f0ba92a5bd237e399433f3181b6d1ddbbdfab8a485d4a02639cb9a4ee601d`

```dockerfile
```

-	Layers:
	-	`sha256:c2834bb66618172f229e2ab92f8944468c3565a30ca12170c67f6d2cf69edc0b`  
		Last Modified: Thu, 04 Sep 2025 00:45:51 GMT  
		Size: 5.5 MB (5538500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5996fd8bb0600585c1089f8c81d3d8669e19b575e61e7fd5068bbeb6c55e6370`  
		Last Modified: Thu, 04 Sep 2025 00:45:51 GMT  
		Size: 29.1 KB (29055 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130` - linux; s390x

```console
$ docker pull ghost@sha256:01a31d1ac0f77574956342cb049e74b910d8816010d659f6bb78bc6092f4f325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204963295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2c96b382e65462523b7e154bdce6c50dba0981548c3eeffeb1627f8709c530`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 13 Aug 2025 02:19:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dadfc3ada3cd4f49e71dc39867db6cf8d4c2cb806f817ea84710057fd1995b`  
		Last Modified: Wed, 13 Aug 2025 15:28:53 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cf7bcb01d49fe8baaafab6d3baac3b451acab827c4ad06b02e9d3ae34486bd`  
		Last Modified: Wed, 03 Sep 2025 22:06:16 GMT  
		Size: 41.2 MB (41222537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89207a8592308cc545b6f73e5a3c4b6aa3204af29454a72ce9f19bf9df3ba5a1`  
		Last Modified: Wed, 03 Sep 2025 22:06:14 GMT  
		Size: 1.7 MB (1712554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac75b645d2254afb8a4f6736b609714f769375ae1e31bf9d2499cf6023437b17`  
		Last Modified: Wed, 03 Sep 2025 22:06:14 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c84a8ea6c419a5caad58c4a291506de73829b25915d2bebc5a61a6c161434d`  
		Last Modified: Wed, 03 Sep 2025 22:18:51 GMT  
		Size: 1.4 MB (1410230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee2e3a4f2ccfcbb5166e0952374fcc01b7420e3d1fda8293bc33805424deec1`  
		Last Modified: Wed, 03 Sep 2025 22:18:52 GMT  
		Size: 11.1 MB (11071555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13de54eaa4dae667fc0e76b0dd29b72ceff3e31a12dcfd009f0c69fd459b0b4`  
		Last Modified: Wed, 03 Sep 2025 22:19:00 GMT  
		Size: 122.7 MB (122654261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d998a9c8c5247811966fbb13d5e0faea9447fa214df71570c6c262a0ef3ac43a`  
		Last Modified: Wed, 03 Sep 2025 22:18:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130` - unknown; unknown

```console
$ docker pull ghost@sha256:945143e3f85e3d08b620946893f48235d4405b1e0ff8a827a379b40b09de105d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67138c2398e29bed49646c1f27a1eb1c889df60026e213e5df07e73a25016e0`

```dockerfile
```

-	Layers:
	-	`sha256:6a5c44e5d19caa1efa403ff4c6a8a68cb350bfc3bed36a3656d3ecee994840ad`  
		Last Modified: Thu, 04 Sep 2025 00:45:56 GMT  
		Size: 5.5 MB (5532478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba483f5452f593bb948fbf74c1106fe761e2c505fbe45c86c501f3d187d4780`  
		Last Modified: Thu, 04 Sep 2025 00:45:57 GMT  
		Size: 29.0 KB (29013 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130-alpine`

```console
$ docker pull ghost@sha256:cac8c28d63e68edcfd80389c97fc256da20d897e3d0901ec6b05618e54800e64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:d5cb0f8f3cd02fbb62bdc4b981bcda5c4e7206947353aca440e42bd80e14176b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166807509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d63f9cdba50d85f6e1ba2a8ee7be2beb4910cbea7795fea16de2a99f9039cd7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88300f8759af46375ccc157a0a0dbf7cdaeded52394b5ce2ce074e3b773fe82`  
		Last Modified: Wed, 03 Sep 2025 20:29:11 GMT  
		Size: 42.8 MB (42750733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd345d7e43c58474c833bee593321ab1097dd720bebd8032e75fbf5b81b1e554`  
		Last Modified: Wed, 03 Sep 2025 20:29:08 GMT  
		Size: 1.3 MB (1260576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de821d16564893ff12fae9499550711d92157ed1e6705a8c7f7e63eac0a2bb9`  
		Last Modified: Wed, 03 Sep 2025 20:29:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089ecb353a985c02c4a60ed3b041ab383897fb1212e1e951bb2a8583e41267ff`  
		Last Modified: Wed, 03 Sep 2025 21:10:13 GMT  
		Size: 777.0 KB (777041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35313b08dcca3c86127d0c0678c3ae54dd558ec22f1d6e1343e305ee0c70e7ca`  
		Last Modified: Wed, 03 Sep 2025 21:10:13 GMT  
		Size: 1.1 MB (1119667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7bd0e2cf124c7cee51b79233f00ad9e2f6e33a1e0544d0c110a8453f5da3d2`  
		Last Modified: Wed, 03 Sep 2025 21:10:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f0a4ecf244cac89f2fa466907d39436d5d662f7b08b134afbd5979da9a079a`  
		Last Modified: Wed, 03 Sep 2025 21:10:15 GMT  
		Size: 11.1 MB (11072137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f2ff5a9280ad28a3d710c276bbe41118b4e2e68cb842697713da95cc20d0ff`  
		Last Modified: Wed, 03 Sep 2025 21:10:34 GMT  
		Size: 106.0 MB (106026471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29306af234df90804ed2099ce58608a6bccf8080f4e6a6c02cd565b8f9225aad`  
		Last Modified: Wed, 03 Sep 2025 21:10:15 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:bfc4cc04127df728a9f1562c7c9813af6b5cb8b190d7accff3b68204fdb8d60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fc59a7dcfa9d13a70c596dc3c5f94d22333aaa5e3f0ff7b13abda182bbfc93`

```dockerfile
```

-	Layers:
	-	`sha256:ba0df3526181df2df82c1e7eff6ae08dd49fe5bf894a45ec15d05c887165da9c`  
		Last Modified: Thu, 04 Sep 2025 00:45:49 GMT  
		Size: 3.3 MB (3327656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ede73372ba139363feb614fba3ff6becb8c77d15039798d9c520bca242986aef`  
		Last Modified: Thu, 04 Sep 2025 00:45:50 GMT  
		Size: 32.0 KB (31987 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:eb608fa4cda5d74361522caa0401b8c5bd901b5808a7d049b696163e057d82ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179432613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f107b730fbb85bc5f80d625c10bbc5dc3b31e0c7e46823bcab3d669ec4481f41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c533aeba408974e594ea5abca2331989c4f9224b40535f05cb74268ac2ee5bd2`  
		Last Modified: Wed, 03 Sep 2025 22:10:49 GMT  
		Size: 41.0 MB (41036904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bef4fd64b731a7dbaa685234c290f08ea5fb12da71db7f2c3cc63c5cea422b`  
		Last Modified: Wed, 03 Sep 2025 22:10:44 GMT  
		Size: 1.3 MB (1260557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd71b6fecbcefd165694195568ae1093f182b78f1e5400e966ebce9e19df23b`  
		Last Modified: Wed, 03 Sep 2025 22:10:44 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9568b30b545fbb29f4e949ac3df28c4d652eb2c8423f3818b7d68adc28c73485`  
		Last Modified: Wed, 03 Sep 2025 23:17:44 GMT  
		Size: 766.1 KB (766086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a3a09e68a81b9a49664458407175080bd86669aa7e1ddbb79c86a9edef5f8e`  
		Last Modified: Wed, 03 Sep 2025 23:17:44 GMT  
		Size: 1.1 MB (1086411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2087e84578591d1182129c1935e1e80d59544000e520cad85100654e531b87e7`  
		Last Modified: Wed, 03 Sep 2025 23:17:45 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64996ebfc19e794d4de26f10611c5dc41e98c0b2470e602b28a1422d333fce23`  
		Last Modified: Wed, 03 Sep 2025 23:17:46 GMT  
		Size: 11.1 MB (11082699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d7126551ddbccc7aee0df08f2ca21a2407f38ca2895a37d5e0a526c257d585`  
		Last Modified: Wed, 03 Sep 2025 23:17:56 GMT  
		Size: 120.7 MB (120697857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff05f03661b17772c3de3233f5ddcd5b108277eb52319a4ba577e00eab40f23a`  
		Last Modified: Wed, 03 Sep 2025 23:17:45 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:7ea2fd9bd3623fa274acb0e4e31fbd8450785b8e08bd4758421daeb2309b885f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd70712c1d84e9a9e9797ea74eecfcd64c054d7103ac3867b65178270e94ce7d`

```dockerfile
```

-	Layers:
	-	`sha256:b1ce8690c10988ee5220caa608171cb2b9800f1023a3ad555fed93708ea8a30a`  
		Last Modified: Thu, 04 Sep 2025 00:45:54 GMT  
		Size: 31.9 KB (31893 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:bbf54f2a88185368d6fe7a7077889a80b6065388e5438e6fdc7e8e8795a9ecad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 MB (178243186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79413a928959c779c960d662180b5624f36cccaaa14745868b26e541644b2089`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb4140b5e03430fe1f2e569e8dc5530627a98d42bc658ef64673aa619e6f27`  
		Last Modified: Wed, 03 Sep 2025 22:11:44 GMT  
		Size: 40.5 MB (40493858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddfda3d4b1769d00c0ce7b336b8c0013e9478a7849f8e683a838fd8028725c9`  
		Last Modified: Wed, 03 Sep 2025 22:11:42 GMT  
		Size: 1.3 MB (1260551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43288fb01db5bf2af65a1de4e1bea8a08196ea5a31d3085a15aac9fde3c93c15`  
		Last Modified: Wed, 03 Sep 2025 22:11:41 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce0b0631776b8d519e672b262851fddb80995f34c40bdf40867d3f63104ec73`  
		Last Modified: Wed, 03 Sep 2025 23:22:54 GMT  
		Size: 701.5 KB (701475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e390b9e175abedc487f7869760481fe395f2cc0b37fc4370717e8ce583d9c9`  
		Last Modified: Wed, 03 Sep 2025 23:22:54 GMT  
		Size: 1.1 MB (1086407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e0dbc2769f9074ade9083fba7b88217de9fb05be2140b24f4da459622ea3ff`  
		Last Modified: Wed, 03 Sep 2025 23:22:54 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4d28d97547cd4de17234ede1aa07b4f4a56c3a5fcb0d5e895b9d27c40307`  
		Last Modified: Wed, 03 Sep 2025 23:22:57 GMT  
		Size: 11.1 MB (11071916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43f0c035cc1987950b4c72bab9c8e8c64badb4056ae9437a10debc97edb99fd`  
		Last Modified: Wed, 03 Sep 2025 23:23:03 GMT  
		Size: 120.4 MB (120408752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872fedc0aca5a893792a516ace674d63d54e472ce23f5a9802499d62dabe450a`  
		Last Modified: Wed, 03 Sep 2025 23:22:56 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:dcc187cc6bba04ede3816939db84a0595a822a08dafff3dfada952b5f5253ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3356777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04351db5cb4c7abcaef6c0716b47986c5e829791e0525b9631f64beec54f8b7c`

```dockerfile
```

-	Layers:
	-	`sha256:e74f62c324b176ee0cc3e1ad57c06ce75bb8c79e57e088c1926a7803136d677b`  
		Last Modified: Thu, 04 Sep 2025 00:45:58 GMT  
		Size: 3.3 MB (3324669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:091a419f9643fda9b99bdb6d8f0870dee80ba13da022784ee9af36094a6a4714`  
		Last Modified: Thu, 04 Sep 2025 00:45:59 GMT  
		Size: 32.1 KB (32108 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:3cec8973df5e31133d48aca400a8e43d5e1ce88c9528afe97b906e67e95395ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186298708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1daa1350bc99bd62f406f70768fe4297637b70e22803c42846e187098305d65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8e8228254a218fbf68fbf8d7093ea99dfce63dd0a72ad0cc8be65e6da3f7c8`  
		Last Modified: Wed, 03 Sep 2025 21:21:49 GMT  
		Size: 42.4 MB (42433073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c149c7c96aa9b49de8c5de3415d3692e81ced50773077ea0be1a0f3f36032234`  
		Last Modified: Wed, 03 Sep 2025 21:21:43 GMT  
		Size: 1.3 MB (1260573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127c05f5df6b075d5c314444a05d3de523268e2de5e9b235e7ba72aa60ed3c61`  
		Last Modified: Wed, 03 Sep 2025 21:21:43 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21a07352734c4f136c142d20b2cf994e5c6256385e224650deceb893f8d1b33`  
		Last Modified: Wed, 03 Sep 2025 22:17:00 GMT  
		Size: 838.6 KB (838576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28887b48c1997751c390dfc44704bda2dfe64d584b7b896595205e775066555c`  
		Last Modified: Wed, 03 Sep 2025 22:17:00 GMT  
		Size: 1.0 MB (1046721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5038a642123ae385b43d639ceb0b1d84fbae53e1c8aaebca3e0c5c9975da26`  
		Last Modified: Wed, 03 Sep 2025 22:17:00 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc4259dbd9c5928cef457319ce2222df4d97405cfebce48325f9038f8c6eaa0`  
		Last Modified: Wed, 03 Sep 2025 22:17:01 GMT  
		Size: 11.1 MB (11071509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55c51524d86fda2d1932ac29d7009e00aeb4e55f03aeb9fa55b66d11a8db22a`  
		Last Modified: Wed, 03 Sep 2025 22:17:23 GMT  
		Size: 125.5 MB (125516320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7417398f7cf371a2155a9c915c915945a4003ed24b0fd70648677673f048fec0`  
		Last Modified: Wed, 03 Sep 2025 22:17:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:b0f4847bc476a97f5630ffe64aff4d265cf6c02f71036715479c30b58437d35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3193e302105b224bd96838e7c3371ebf087b18a4f4821d7a8509607930e0dce8`

```dockerfile
```

-	Layers:
	-	`sha256:5f81bf1bb62eac5fe1d84c2a4e23c6f6a82791b8690b90b8ea07f226b0fc4e2b`  
		Last Modified: Thu, 04 Sep 2025 00:46:03 GMT  
		Size: 3.3 MB (3327752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32488d9cc32fbc2d3e91e5fd8e0b48d27364010639a77bc88d90cbbadcc6fa25`  
		Last Modified: Thu, 04 Sep 2025 00:46:04 GMT  
		Size: 32.1 KB (32140 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.4`

```console
$ docker pull ghost@sha256:13af85b409bddc414418ed1aefea4339ef11d70b79daaa70cfd8d5ddfed3bde2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:5.130.4` - linux; amd64

```console
$ docker pull ghost@sha256:b708658fb27413945daa9986cf8566160728af899ddf7c449c53a5af5d8a2648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192522180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311211c3d264cee8cda0d7a5fd42bee340a61435ef298ac295bcd1ae03678e79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 13 Aug 2025 02:19:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4733cb89761b11d3b538fd74d6219198e0dd771200912407122d14b2670815`  
		Last Modified: Wed, 03 Sep 2025 21:07:39 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da230fee1a10de928e261cc92d3372d190cd29ea0e6f71177a6987a382b87e4`  
		Last Modified: Wed, 03 Sep 2025 21:07:41 GMT  
		Size: 41.0 MB (40977768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf37311b43e9505cacdcd82aa37169cc3f42aacb75a163605e9092ba8bdf11d`  
		Last Modified: Wed, 03 Sep 2025 21:07:39 GMT  
		Size: 1.7 MB (1712561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d3f25a0e331e1f50f1b678c3a29ae5279356d8999e87b4d7d8e95aaa11c9d3`  
		Last Modified: Wed, 03 Sep 2025 21:07:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cffbf174346f17c550affa3240baf4f0197bb0584b5e2076026c9229b5a2b29`  
		Last Modified: Wed, 03 Sep 2025 21:10:12 GMT  
		Size: 1.4 MB (1444930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099260993daa4dd7302111064c0de72604fca27ee27010a390a6ad084dbc78f2`  
		Last Modified: Wed, 03 Sep 2025 21:10:14 GMT  
		Size: 11.1 MB (11071502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3d719ab3e4524b94610a70a2718437cc14d2b80e4d94163c22060864f40f69`  
		Last Modified: Wed, 03 Sep 2025 21:10:28 GMT  
		Size: 109.1 MB (109080828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e128a7c9170bcca829336cf757a1d74c66b79af3b1530a151b15e4b839a3b5`  
		Last Modified: Wed, 03 Sep 2025 21:10:13 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.4` - unknown; unknown

```console
$ docker pull ghost@sha256:b0f2dfb0b5ba70239b1b38c7c5369b4b57ece9414ad04a4e96912af9120b5c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6750e7db3f4f9aa29a29194a9c75007212824f1568a8b9b8cc69dd7043f071fa`

```dockerfile
```

-	Layers:
	-	`sha256:081f84e98559d922114e02ecf535d591da789e0b7143ae439100d1c5db66c9d6`  
		Last Modified: Thu, 04 Sep 2025 00:45:32 GMT  
		Size: 5.5 MB (5538655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c21ce37cd62b0c0508f834423979ee495d99d198be06e86ae8e83d22977c163`  
		Last Modified: Thu, 04 Sep 2025 00:45:33 GMT  
		Size: 29.0 KB (29014 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.4` - linux; arm variant v7

```console
$ docker pull ghost@sha256:3c6241cd855b10132734a41e49c6f91f5a03b4d037f1855dec023b0b04cbd49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195794297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37188079b442f39faf8a080eb082291f4f6329525b8f000f10b24a791f48fc3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 13 Aug 2025 02:19:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae1e510a43ef8f416095b11f0182b2e280a16abb567ffe9973ee818f1ced070`  
		Last Modified: Wed, 13 Aug 2025 00:43:01 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4bcd4f3d11b003db3518f4a0713f95cc798b21c548a3ccd283119d9444fe49`  
		Last Modified: Wed, 03 Sep 2025 22:14:13 GMT  
		Size: 37.1 MB (37064132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fc96186c22f4a3af271347e6c955d9498ea60891c5d38188dac326ee76c7d0`  
		Last Modified: Wed, 03 Sep 2025 22:14:05 GMT  
		Size: 1.7 MB (1712733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c993896595cfc57bb020e68783a9a2081ea6e5c5d4580a8cbaf6a2f395acc903`  
		Last Modified: Wed, 03 Sep 2025 22:14:04 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e408b2e58ff20b50d8d71dfb4c8f2129b89ddb236d51e9299bc46185934c8f3`  
		Last Modified: Wed, 03 Sep 2025 23:16:09 GMT  
		Size: 1.4 MB (1412584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346c9c473548776cd17836990f8faae75f71272a59a19233b76019268ddbbe22`  
		Last Modified: Wed, 03 Sep 2025 23:16:11 GMT  
		Size: 11.1 MB (11071877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8c8a7bf8dcad2a81142b0cc770783f8379e3a4d32a33476c1395c193e1183a`  
		Last Modified: Wed, 03 Sep 2025 23:16:27 GMT  
		Size: 120.6 MB (120589709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef19e20e6c283d2aea4572b2e99069d772a7186734116df72d083c53e397d560`  
		Last Modified: Wed, 03 Sep 2025 23:16:09 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.4` - unknown; unknown

```console
$ docker pull ghost@sha256:f7ed0fc59cb0df448a75ef934c18d9e25909f88361afd976396cd683979c9ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5570518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df583ee60a866f3fd11f1ef29901f2243172279f666956c97c4d4305cf9be344`

```dockerfile
```

-	Layers:
	-	`sha256:810f1412a453a102f19703c7dc1bbc386910c7a84edcb0abf5247d4b3f249046`  
		Last Modified: Thu, 04 Sep 2025 00:45:39 GMT  
		Size: 5.5 MB (5541410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3349d4ae03f9717f2633f767770ea5ca5b2668104538fa49692f2c08682a34b`  
		Last Modified: Thu, 04 Sep 2025 00:45:40 GMT  
		Size: 29.1 KB (29108 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.4` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:a91eb3665ee3884b833b83e6cf8b191ab575481f77744638424f53aace422170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192375878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03aeb5fd265f63a7b8ec1a4cfb86aa20ac7660fdb131493a799549cb3345b7c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 13 Aug 2025 02:19:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27263372d67228bb86c6e522c8fc32c5e6a4a10ddabec215fa8026f3d01a3508`  
		Last Modified: Thu, 28 Aug 2025 14:40:51 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2518670ec6f69a0f47a52c0f889152d9f59f5696aea4f65c7738975a3ff4fac6`  
		Last Modified: Wed, 03 Sep 2025 21:23:49 GMT  
		Size: 40.9 MB (40939649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bded516fefd7eab843a38696ab759387eea7ef0a141a2f721999709cfd27e53f`  
		Last Modified: Wed, 03 Sep 2025 21:23:45 GMT  
		Size: 1.7 MB (1712624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c59bbf66433150dcfe0f4cff482e662861d1b5087f97754c55c1dccd1c233f4`  
		Last Modified: Wed, 03 Sep 2025 21:23:45 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eefb2b1951c8ff402843632e7f613eed2998393b4737a4a078aea9be891a32e`  
		Last Modified: Wed, 03 Sep 2025 22:12:58 GMT  
		Size: 1.4 MB (1376742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2255fdd165f93bc1f5313ac8023807e7d638bc3655afa084bff339792392a5`  
		Last Modified: Wed, 03 Sep 2025 22:13:01 GMT  
		Size: 11.1 MB (11071993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4190b44a91f23582dd26283fbe5168cad1d34efb257b71d338f84fc10e7249`  
		Last Modified: Wed, 03 Sep 2025 22:13:06 GMT  
		Size: 109.2 MB (109188537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61dcdf8f271e5a205e84daaa269033d79d461e7f09835b556b67bb2bbaefe85c`  
		Last Modified: Wed, 03 Sep 2025 22:13:00 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.4` - unknown; unknown

```console
$ docker pull ghost@sha256:f531c8a9df549c87b2243de5b8e58d1c47b9012ee0d164982b814a287fcf3b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c821b8e1d532126f3afcf67891ea7dc3b6faabadba0543cb8e5338658a3186e`

```dockerfile
```

-	Layers:
	-	`sha256:186f5ea75fc4e6968575aed2e85344bf7326652cf9d2ee16f6aab9bab7d9e48f`  
		Last Modified: Thu, 04 Sep 2025 00:45:45 GMT  
		Size: 5.5 MB (5538946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9c8867ad1537600d462622e255fabed6eb6c00a639fb44f0131731a576ce87`  
		Last Modified: Thu, 04 Sep 2025 00:45:46 GMT  
		Size: 29.1 KB (29136 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.4` - linux; ppc64le

```console
$ docker pull ghost@sha256:5eef4c5fe4b005f7fbbbd12af9ecb44d636a9b72e22224e377cde56547a295d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.2 MB (213213895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407c5f3d8a8cbfeefb5113c4f4ea32a13dabbc03cb16d7a54711da80d616b289`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 13 Aug 2025 02:19:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db49890cc93d9412b095c6d9e7c7dcd1224e0b5c93c9c8848c12d48ecffbb89a`  
		Last Modified: Wed, 13 Aug 2025 13:16:33 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82069806ce067cfe764da9862c1d3880e4de07fe659a1dcc35e05a5f703b380c`  
		Last Modified: Wed, 03 Sep 2025 23:07:26 GMT  
		Size: 43.5 MB (43469521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dcae3e4550644ec520c3da3c7a5351ffef1ea4e938911c0bc6883e648dc493`  
		Last Modified: Wed, 03 Sep 2025 21:58:55 GMT  
		Size: 1.7 MB (1712746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f616b2d0e663d180ffc95a63e2a12c2bb578e3ef724f5357d6459c02c587bfb`  
		Last Modified: Wed, 03 Sep 2025 21:58:56 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48f0afd3003f91fda85b8fa35aa74ef1071291c271c7d295a0b381d437e25a6`  
		Last Modified: Wed, 03 Sep 2025 22:21:06 GMT  
		Size: 1.4 MB (1366801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab475f2027f5e7e7387b4cadf343389a0494b8ce0a437a02f629fef42f3951b5`  
		Last Modified: Wed, 03 Sep 2025 22:21:08 GMT  
		Size: 11.1 MB (11071290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c00f4dc7cfca47161dc50f5e811aa0b1b5a24604f2e458e3637c7bcce0dbc0e`  
		Last Modified: Wed, 03 Sep 2025 22:21:20 GMT  
		Size: 123.5 MB (123515780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc301d8e0285057786e500c0dd71d20c458646631597b52bd6a200df5690504c`  
		Last Modified: Wed, 03 Sep 2025 22:21:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.4` - unknown; unknown

```console
$ docker pull ghost@sha256:5628823fd20dfac1fe25ac5bf5e52b514139c5b17c29f5d2b11422105bf6616b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8f0ba92a5bd237e399433f3181b6d1ddbbdfab8a485d4a02639cb9a4ee601d`

```dockerfile
```

-	Layers:
	-	`sha256:c2834bb66618172f229e2ab92f8944468c3565a30ca12170c67f6d2cf69edc0b`  
		Last Modified: Thu, 04 Sep 2025 00:45:51 GMT  
		Size: 5.5 MB (5538500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5996fd8bb0600585c1089f8c81d3d8669e19b575e61e7fd5068bbeb6c55e6370`  
		Last Modified: Thu, 04 Sep 2025 00:45:51 GMT  
		Size: 29.1 KB (29055 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.4` - linux; s390x

```console
$ docker pull ghost@sha256:01a31d1ac0f77574956342cb049e74b910d8816010d659f6bb78bc6092f4f325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204963295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2c96b382e65462523b7e154bdce6c50dba0981548c3eeffeb1627f8709c530`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 13 Aug 2025 02:19:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dadfc3ada3cd4f49e71dc39867db6cf8d4c2cb806f817ea84710057fd1995b`  
		Last Modified: Wed, 13 Aug 2025 15:28:53 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cf7bcb01d49fe8baaafab6d3baac3b451acab827c4ad06b02e9d3ae34486bd`  
		Last Modified: Wed, 03 Sep 2025 22:06:16 GMT  
		Size: 41.2 MB (41222537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89207a8592308cc545b6f73e5a3c4b6aa3204af29454a72ce9f19bf9df3ba5a1`  
		Last Modified: Wed, 03 Sep 2025 22:06:14 GMT  
		Size: 1.7 MB (1712554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac75b645d2254afb8a4f6736b609714f769375ae1e31bf9d2499cf6023437b17`  
		Last Modified: Wed, 03 Sep 2025 22:06:14 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c84a8ea6c419a5caad58c4a291506de73829b25915d2bebc5a61a6c161434d`  
		Last Modified: Wed, 03 Sep 2025 22:18:51 GMT  
		Size: 1.4 MB (1410230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee2e3a4f2ccfcbb5166e0952374fcc01b7420e3d1fda8293bc33805424deec1`  
		Last Modified: Wed, 03 Sep 2025 22:18:52 GMT  
		Size: 11.1 MB (11071555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13de54eaa4dae667fc0e76b0dd29b72ceff3e31a12dcfd009f0c69fd459b0b4`  
		Last Modified: Wed, 03 Sep 2025 22:19:00 GMT  
		Size: 122.7 MB (122654261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d998a9c8c5247811966fbb13d5e0faea9447fa214df71570c6c262a0ef3ac43a`  
		Last Modified: Wed, 03 Sep 2025 22:18:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.4` - unknown; unknown

```console
$ docker pull ghost@sha256:945143e3f85e3d08b620946893f48235d4405b1e0ff8a827a379b40b09de105d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67138c2398e29bed49646c1f27a1eb1c889df60026e213e5df07e73a25016e0`

```dockerfile
```

-	Layers:
	-	`sha256:6a5c44e5d19caa1efa403ff4c6a8a68cb350bfc3bed36a3656d3ecee994840ad`  
		Last Modified: Thu, 04 Sep 2025 00:45:56 GMT  
		Size: 5.5 MB (5532478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba483f5452f593bb948fbf74c1106fe761e2c505fbe45c86c501f3d187d4780`  
		Last Modified: Thu, 04 Sep 2025 00:45:57 GMT  
		Size: 29.0 KB (29013 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:5.130.4-alpine`

```console
$ docker pull ghost@sha256:cac8c28d63e68edcfd80389c97fc256da20d897e3d0901ec6b05618e54800e64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:5.130.4-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:d5cb0f8f3cd02fbb62bdc4b981bcda5c4e7206947353aca440e42bd80e14176b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166807509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d63f9cdba50d85f6e1ba2a8ee7be2beb4910cbea7795fea16de2a99f9039cd7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88300f8759af46375ccc157a0a0dbf7cdaeded52394b5ce2ce074e3b773fe82`  
		Last Modified: Wed, 03 Sep 2025 20:29:11 GMT  
		Size: 42.8 MB (42750733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd345d7e43c58474c833bee593321ab1097dd720bebd8032e75fbf5b81b1e554`  
		Last Modified: Wed, 03 Sep 2025 20:29:08 GMT  
		Size: 1.3 MB (1260576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de821d16564893ff12fae9499550711d92157ed1e6705a8c7f7e63eac0a2bb9`  
		Last Modified: Wed, 03 Sep 2025 20:29:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089ecb353a985c02c4a60ed3b041ab383897fb1212e1e951bb2a8583e41267ff`  
		Last Modified: Wed, 03 Sep 2025 21:10:13 GMT  
		Size: 777.0 KB (777041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35313b08dcca3c86127d0c0678c3ae54dd558ec22f1d6e1343e305ee0c70e7ca`  
		Last Modified: Wed, 03 Sep 2025 21:10:13 GMT  
		Size: 1.1 MB (1119667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7bd0e2cf124c7cee51b79233f00ad9e2f6e33a1e0544d0c110a8453f5da3d2`  
		Last Modified: Wed, 03 Sep 2025 21:10:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f0a4ecf244cac89f2fa466907d39436d5d662f7b08b134afbd5979da9a079a`  
		Last Modified: Wed, 03 Sep 2025 21:10:15 GMT  
		Size: 11.1 MB (11072137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f2ff5a9280ad28a3d710c276bbe41118b4e2e68cb842697713da95cc20d0ff`  
		Last Modified: Wed, 03 Sep 2025 21:10:34 GMT  
		Size: 106.0 MB (106026471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29306af234df90804ed2099ce58608a6bccf8080f4e6a6c02cd565b8f9225aad`  
		Last Modified: Wed, 03 Sep 2025 21:10:15 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.4-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:bfc4cc04127df728a9f1562c7c9813af6b5cb8b190d7accff3b68204fdb8d60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fc59a7dcfa9d13a70c596dc3c5f94d22333aaa5e3f0ff7b13abda182bbfc93`

```dockerfile
```

-	Layers:
	-	`sha256:ba0df3526181df2df82c1e7eff6ae08dd49fe5bf894a45ec15d05c887165da9c`  
		Last Modified: Thu, 04 Sep 2025 00:45:49 GMT  
		Size: 3.3 MB (3327656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ede73372ba139363feb614fba3ff6becb8c77d15039798d9c520bca242986aef`  
		Last Modified: Thu, 04 Sep 2025 00:45:50 GMT  
		Size: 32.0 KB (31987 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.4-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:eb608fa4cda5d74361522caa0401b8c5bd901b5808a7d049b696163e057d82ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179432613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f107b730fbb85bc5f80d625c10bbc5dc3b31e0c7e46823bcab3d669ec4481f41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c533aeba408974e594ea5abca2331989c4f9224b40535f05cb74268ac2ee5bd2`  
		Last Modified: Wed, 03 Sep 2025 22:10:49 GMT  
		Size: 41.0 MB (41036904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bef4fd64b731a7dbaa685234c290f08ea5fb12da71db7f2c3cc63c5cea422b`  
		Last Modified: Wed, 03 Sep 2025 22:10:44 GMT  
		Size: 1.3 MB (1260557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd71b6fecbcefd165694195568ae1093f182b78f1e5400e966ebce9e19df23b`  
		Last Modified: Wed, 03 Sep 2025 22:10:44 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9568b30b545fbb29f4e949ac3df28c4d652eb2c8423f3818b7d68adc28c73485`  
		Last Modified: Wed, 03 Sep 2025 23:17:44 GMT  
		Size: 766.1 KB (766086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a3a09e68a81b9a49664458407175080bd86669aa7e1ddbb79c86a9edef5f8e`  
		Last Modified: Wed, 03 Sep 2025 23:17:44 GMT  
		Size: 1.1 MB (1086411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2087e84578591d1182129c1935e1e80d59544000e520cad85100654e531b87e7`  
		Last Modified: Wed, 03 Sep 2025 23:17:45 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64996ebfc19e794d4de26f10611c5dc41e98c0b2470e602b28a1422d333fce23`  
		Last Modified: Wed, 03 Sep 2025 23:17:46 GMT  
		Size: 11.1 MB (11082699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d7126551ddbccc7aee0df08f2ca21a2407f38ca2895a37d5e0a526c257d585`  
		Last Modified: Wed, 03 Sep 2025 23:17:56 GMT  
		Size: 120.7 MB (120697857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff05f03661b17772c3de3233f5ddcd5b108277eb52319a4ba577e00eab40f23a`  
		Last Modified: Wed, 03 Sep 2025 23:17:45 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.4-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:7ea2fd9bd3623fa274acb0e4e31fbd8450785b8e08bd4758421daeb2309b885f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd70712c1d84e9a9e9797ea74eecfcd64c054d7103ac3867b65178270e94ce7d`

```dockerfile
```

-	Layers:
	-	`sha256:b1ce8690c10988ee5220caa608171cb2b9800f1023a3ad555fed93708ea8a30a`  
		Last Modified: Thu, 04 Sep 2025 00:45:54 GMT  
		Size: 31.9 KB (31893 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.4-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:bbf54f2a88185368d6fe7a7077889a80b6065388e5438e6fdc7e8e8795a9ecad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 MB (178243186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79413a928959c779c960d662180b5624f36cccaaa14745868b26e541644b2089`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb4140b5e03430fe1f2e569e8dc5530627a98d42bc658ef64673aa619e6f27`  
		Last Modified: Wed, 03 Sep 2025 22:11:44 GMT  
		Size: 40.5 MB (40493858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddfda3d4b1769d00c0ce7b336b8c0013e9478a7849f8e683a838fd8028725c9`  
		Last Modified: Wed, 03 Sep 2025 22:11:42 GMT  
		Size: 1.3 MB (1260551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43288fb01db5bf2af65a1de4e1bea8a08196ea5a31d3085a15aac9fde3c93c15`  
		Last Modified: Wed, 03 Sep 2025 22:11:41 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce0b0631776b8d519e672b262851fddb80995f34c40bdf40867d3f63104ec73`  
		Last Modified: Wed, 03 Sep 2025 23:22:54 GMT  
		Size: 701.5 KB (701475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e390b9e175abedc487f7869760481fe395f2cc0b37fc4370717e8ce583d9c9`  
		Last Modified: Wed, 03 Sep 2025 23:22:54 GMT  
		Size: 1.1 MB (1086407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e0dbc2769f9074ade9083fba7b88217de9fb05be2140b24f4da459622ea3ff`  
		Last Modified: Wed, 03 Sep 2025 23:22:54 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e4d28d97547cd4de17234ede1aa07b4f4a56c3a5fcb0d5e895b9d27c40307`  
		Last Modified: Wed, 03 Sep 2025 23:22:57 GMT  
		Size: 11.1 MB (11071916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43f0c035cc1987950b4c72bab9c8e8c64badb4056ae9437a10debc97edb99fd`  
		Last Modified: Wed, 03 Sep 2025 23:23:03 GMT  
		Size: 120.4 MB (120408752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872fedc0aca5a893792a516ace674d63d54e472ce23f5a9802499d62dabe450a`  
		Last Modified: Wed, 03 Sep 2025 23:22:56 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.4-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:dcc187cc6bba04ede3816939db84a0595a822a08dafff3dfada952b5f5253ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3356777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04351db5cb4c7abcaef6c0716b47986c5e829791e0525b9631f64beec54f8b7c`

```dockerfile
```

-	Layers:
	-	`sha256:e74f62c324b176ee0cc3e1ad57c06ce75bb8c79e57e088c1926a7803136d677b`  
		Last Modified: Thu, 04 Sep 2025 00:45:58 GMT  
		Size: 3.3 MB (3324669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:091a419f9643fda9b99bdb6d8f0870dee80ba13da022784ee9af36094a6a4714`  
		Last Modified: Thu, 04 Sep 2025 00:45:59 GMT  
		Size: 32.1 KB (32108 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5.130.4-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:3cec8973df5e31133d48aca400a8e43d5e1ce88c9528afe97b906e67e95395ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186298708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1daa1350bc99bd62f406f70768fe4297637b70e22803c42846e187098305d65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_VERSION=20.19.5
# Wed, 13 Aug 2025 02:19:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="3ea6ae2833f2d75e4d84731a9c01f50eff5198d78f724fa673281468e1c2077b" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV YARN_VERSION=1.22.22
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node"]
# Wed, 13 Aug 2025 02:19:16 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV NODE_ENV=production
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 13 Aug 2025 02:19:16 GMT
ENV GHOST_VERSION=5.130.4
# Wed, 13 Aug 2025 02:19:16 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
WORKDIR /var/lib/ghost
# Wed, 13 Aug 2025 02:19:16 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 13 Aug 2025 02:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 13 Aug 2025 02:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 02:19:16 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 13 Aug 2025 02:19:16 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8e8228254a218fbf68fbf8d7093ea99dfce63dd0a72ad0cc8be65e6da3f7c8`  
		Last Modified: Wed, 03 Sep 2025 21:21:49 GMT  
		Size: 42.4 MB (42433073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c149c7c96aa9b49de8c5de3415d3692e81ced50773077ea0be1a0f3f36032234`  
		Last Modified: Wed, 03 Sep 2025 21:21:43 GMT  
		Size: 1.3 MB (1260573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127c05f5df6b075d5c314444a05d3de523268e2de5e9b235e7ba72aa60ed3c61`  
		Last Modified: Wed, 03 Sep 2025 21:21:43 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21a07352734c4f136c142d20b2cf994e5c6256385e224650deceb893f8d1b33`  
		Last Modified: Wed, 03 Sep 2025 22:17:00 GMT  
		Size: 838.6 KB (838576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28887b48c1997751c390dfc44704bda2dfe64d584b7b896595205e775066555c`  
		Last Modified: Wed, 03 Sep 2025 22:17:00 GMT  
		Size: 1.0 MB (1046721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5038a642123ae385b43d639ceb0b1d84fbae53e1c8aaebca3e0c5c9975da26`  
		Last Modified: Wed, 03 Sep 2025 22:17:00 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc4259dbd9c5928cef457319ce2222df4d97405cfebce48325f9038f8c6eaa0`  
		Last Modified: Wed, 03 Sep 2025 22:17:01 GMT  
		Size: 11.1 MB (11071509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55c51524d86fda2d1932ac29d7009e00aeb4e55f03aeb9fa55b66d11a8db22a`  
		Last Modified: Wed, 03 Sep 2025 22:17:23 GMT  
		Size: 125.5 MB (125516320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7417398f7cf371a2155a9c915c915945a4003ed24b0fd70648677673f048fec0`  
		Last Modified: Wed, 03 Sep 2025 22:17:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5.130.4-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:b0f4847bc476a97f5630ffe64aff4d265cf6c02f71036715479c30b58437d35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3193e302105b224bd96838e7c3371ebf087b18a4f4821d7a8509607930e0dce8`

```dockerfile
```

-	Layers:
	-	`sha256:5f81bf1bb62eac5fe1d84c2a4e23c6f6a82791b8690b90b8ea07f226b0fc4e2b`  
		Last Modified: Thu, 04 Sep 2025 00:46:03 GMT  
		Size: 3.3 MB (3327752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32488d9cc32fbc2d3e91e5fd8e0b48d27364010639a77bc88d90cbbadcc6fa25`  
		Last Modified: Thu, 04 Sep 2025 00:46:04 GMT  
		Size: 32.1 KB (32140 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6`

```console
$ docker pull ghost@sha256:2faf7cda2bfe29e925e30e14bed5250c6e326c7653a95e9358ff362717dc5b16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:6` - linux; amd64

```console
$ docker pull ghost@sha256:d2254b21222cfabdc215b43c92ac189c2351439a40ecdc83a41700f015f2b20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211763653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19035ba1f754fb7e686e3ead03ac05371fb6ebcb5a594235bb2c1c5cfcbd007d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291fc5dbbd39fe685232627c96a45e68110c8aa46cb7b065f3a72e72cb22c31d`  
		Last Modified: Thu, 28 Aug 2025 23:34:31 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2561d51a4c67aeb839775fbbf9f06e9b8f865499c3974f3b15d8748dcb0760a1`  
		Last Modified: Thu, 28 Aug 2025 23:34:37 GMT  
		Size: 49.0 MB (49010562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e06c1a47e17a8b62c4f581dfdec846741e13dbf17aacd62f8afa6d668d3da31`  
		Last Modified: Thu, 28 Aug 2025 23:34:30 GMT  
		Size: 1.7 MB (1712554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2403c8b76caca8d2d0a53ca1ee2475bbaece39b293a49cfba277b01186986bb8`  
		Last Modified: Thu, 28 Aug 2025 23:34:30 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76afcf2fa61fa51d34175604b2d563cce965bdb65b1c28ffb73a1ebc63e6336`  
		Last Modified: Mon, 01 Sep 2025 22:31:05 GMT  
		Size: 1.4 MB (1444945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799552c8963493fd20a6604b1b78f4ee50584bd1d896cc157402c8077ff42996`  
		Last Modified: Mon, 01 Sep 2025 22:31:09 GMT  
		Size: 11.7 MB (11650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c19a50e28a047b135e0e3ffe1247bfe04bd0fab6bac5514fc9af7d154ec8565`  
		Last Modified: Mon, 01 Sep 2025 22:31:12 GMT  
		Size: 119.7 MB (119710178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bc276376483c6b837fa4a33a535ec5c7d285e6d1bfabbfcfdcdecf51cb6f3a`  
		Last Modified: Mon, 01 Sep 2025 22:31:05 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:b27a6f3720b8114a95d861609f204edb6ef9bd73fae96181e1a5dd45f9fb78e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a940a71b4fd4b3556eb01803ecb6e63b108795778c8545326b7c716c280201f7`

```dockerfile
```

-	Layers:
	-	`sha256:de464b26004e59cf977beb0f3cdaaff38e6b4f0833e766b1c0c2b047b89ab118`  
		Last Modified: Tue, 02 Sep 2025 00:45:38 GMT  
		Size: 5.5 MB (5532017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7237eef19ee9904fb66b59c2b8a3ea69d8f40436b916f5b639aeb4741b3a350b`  
		Last Modified: Tue, 02 Sep 2025 00:45:39 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm variant v7

```console
$ docker pull ghost@sha256:854fbd11e88160c51d9a2d06fe427d25c19c80cf285926b4fdd1bbecdc091f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203413730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd85aabdfbec73ec1790a771dee3d12061381067e87ad6b49b27cf1a6791172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae1e510a43ef8f416095b11f0182b2e280a16abb567ffe9973ee818f1ced070`  
		Last Modified: Wed, 13 Aug 2025 00:43:01 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5468eccc738adf70ee011b01680c456e47dc04f006dcce1b4cadbf6400263`  
		Last Modified: Fri, 29 Aug 2025 02:42:57 GMT  
		Size: 43.9 MB (43916785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb4b0ef6c2bf4f00b489a41c59c1355636508ad8cc8b009def82424800f2d4c`  
		Last Modified: Fri, 29 Aug 2025 02:42:50 GMT  
		Size: 1.7 MB (1712767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1951b39ccaea6be1c5650f48794d2610c4850f7643d2fbdecbabe1dbb6132054`  
		Last Modified: Fri, 29 Aug 2025 02:42:50 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17358ce1624416ef9ff445daec0c5f9d8b56d0dcf1ca981b81d3ad7fdfddfd0b`  
		Last Modified: Fri, 29 Aug 2025 03:47:51 GMT  
		Size: 1.4 MB (1412627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fb3436b4dbb0037988c989c6e85ea687ab350bd9981dbf00903c477c8bafd1`  
		Last Modified: Fri, 29 Aug 2025 03:47:52 GMT  
		Size: 11.6 MB (11639485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e3dae8a2aa6764159cd144d209389eff5907f4f61c783aaa231625e7a8d39d`  
		Last Modified: Mon, 01 Sep 2025 22:36:11 GMT  
		Size: 120.8 MB (120788809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad92ebadf2b39d220609d1b3753b850a1fff3f9a0944a8920801d6ec17ebb6c`  
		Last Modified: Mon, 01 Sep 2025 22:35:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:9529ba666cb089cbee4321c0a853bbfea116482f0bfc39f0ea1d1f6cefdd5b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5564472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbd7cc01bc0a0f2f594146227aff39025b56fa682086132a547991bcd6afdbb`

```dockerfile
```

-	Layers:
	-	`sha256:bf14bc68813c966bbe8b2bf1ff2923aec3ecf68f0da115ce283156657960bc21`  
		Last Modified: Tue, 02 Sep 2025 00:45:44 GMT  
		Size: 5.5 MB (5534784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed46868ea90f3e5060df97e4ec073c47e70f770d42b0965956af5f8151ef7c0`  
		Last Modified: Tue, 02 Sep 2025 00:45:45 GMT  
		Size: 29.7 KB (29688 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:c71869bc85c04ac42db2d0206a23e0a0012e5dd2a6f3a8bad441bbadc3366b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211307491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d142eaca1b337deba2b831de051dfc274ac02c6088a19dfac39171a950b5f0c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27263372d67228bb86c6e522c8fc32c5e6a4a10ddabec215fa8026f3d01a3508`  
		Last Modified: Thu, 28 Aug 2025 14:40:51 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00ca1ce1c92f9f6153143bddfb381c493c0ae26d3bb85f10d228009ea618291`  
		Last Modified: Fri, 29 Aug 2025 01:27:40 GMT  
		Size: 48.7 MB (48681521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cceee3ed04b670a81910ab2d6400463c1c5253f81047942e7ca695dcbc42bef6`  
		Last Modified: Fri, 29 Aug 2025 01:27:34 GMT  
		Size: 1.7 MB (1712586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9a72dac5922748758980697ec36ffe4814be2e61e21f88b48746e419444192`  
		Last Modified: Fri, 29 Aug 2025 01:27:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990af4a1d6f18056eb115744e5360b959441c63cdac3679b104c29158bc34c5a`  
		Last Modified: Fri, 29 Aug 2025 03:09:43 GMT  
		Size: 1.4 MB (1376654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f35bbd74cc54bb41d37d13a7d299015b97e9b215c742395b169e75fab70ca9`  
		Last Modified: Fri, 29 Aug 2025 03:09:44 GMT  
		Size: 11.7 MB (11650392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918212475e1250b79cf2897198ed00dab67b0f619e097d00489a59f905971a9b`  
		Last Modified: Mon, 01 Sep 2025 22:30:55 GMT  
		Size: 119.8 MB (119800006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759453b512e79c73dbad92d0db51da292d1b4736fb10a248267fbaa032a39947`  
		Last Modified: Mon, 01 Sep 2025 22:30:46 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:7ac6757f4114dc2990c62dd5793009785278c231ae38937c309497e88d36c4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f006d48f55bac7ca7915e12a9ca6c807b4d456d546d35e00b9b33e08cfb444a`

```dockerfile
```

-	Layers:
	-	`sha256:58e7d0eba6c644e7892aeecab188ec6b2e049a87cf4c7ba3cfbc24f721d37b4d`  
		Last Modified: Tue, 02 Sep 2025 00:45:50 GMT  
		Size: 5.5 MB (5532320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3aebc011dd0ca39b19da637deef8c255e64868975c603c86bd92ce8927eb314`  
		Last Modified: Tue, 02 Sep 2025 00:45:51 GMT  
		Size: 29.7 KB (29719 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; ppc64le

```console
$ docker pull ghost@sha256:684dad988bcc8867ee4f8dfa11a5310eaa7354dee2421b9b7713092f8ab66e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222396476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b174c7af12f48df75f029d34136182a00026b3cb584437bd99f6200273987d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db49890cc93d9412b095c6d9e7c7dcd1224e0b5c93c9c8848c12d48ecffbb89a`  
		Last Modified: Wed, 13 Aug 2025 13:16:33 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708047d400332a3ac027b4da8af825b8849d7cf6154f691f6b57c08995f18d5b`  
		Last Modified: Fri, 29 Aug 2025 00:58:52 GMT  
		Size: 51.9 MB (51930458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2905170ec9992e7f18c8d6a624109158fc4d528bbdc72a2bf3b6b5e54abeecd`  
		Last Modified: Fri, 29 Aug 2025 00:58:41 GMT  
		Size: 1.7 MB (1712753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa037f1a005a1ed7b76333d54b8874e5001c088200f60fdbf7a8bf41820a22b9`  
		Last Modified: Fri, 29 Aug 2025 00:58:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cca12707d80a0959f9c8c27d84527a6f395d044dbde84ed7dd6ac6581b59623`  
		Last Modified: Fri, 29 Aug 2025 02:23:49 GMT  
		Size: 1.4 MB (1366738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69098d5fc0ba8e36a59d67177ecb88d69fdec43caedb993f113cbe9548c40fb3`  
		Last Modified: Fri, 29 Aug 2025 02:23:51 GMT  
		Size: 11.7 MB (11650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad520b7406424dd17210f7bf38ab76bbe9e87b3d7c03bd5014dece708efcc6b`  
		Last Modified: Mon, 01 Sep 2025 22:38:59 GMT  
		Size: 123.7 MB (123658547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6c3733ec0f123b114febfe29247afaf79eddfd4d2dfef91760a3071c6eb2a6`  
		Last Modified: Mon, 01 Sep 2025 22:38:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:c15a40d0d6240f38fbb67240a90432f06cca341a5b354a228eccd789c82f7e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c3c4216defb2246a1484c7c9923c2f4488015e3a0ca0c16da74179c1546e13`

```dockerfile
```

-	Layers:
	-	`sha256:55084258c84cba53b42a3dbd4c90b1e800fcfe8b5b1c6f943be6bfe1cf04681c`  
		Last Modified: Tue, 02 Sep 2025 00:45:56 GMT  
		Size: 5.5 MB (5531874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fc0054474cfcb15ca29acbded12e51e37f28f9ca1066504c1ff4dc22618766d`  
		Last Modified: Tue, 02 Sep 2025 00:45:57 GMT  
		Size: 29.6 KB (29634 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6` - linux; s390x

```console
$ docker pull ghost@sha256:2fa624f4cf86e0d598710fd73c2f31b01ea41b83e7873a0ef079af1ecfc8a0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213760480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dcfcc37c5081780279297d15452f2a813e05bf8279e865fd109daa980d5b00b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dadfc3ada3cd4f49e71dc39867db6cf8d4c2cb806f817ea84710057fd1995b`  
		Last Modified: Wed, 13 Aug 2025 15:28:53 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3522eaaadd5604724d773f31f0376394ec59311b336e319267f643b81cd1051`  
		Last Modified: Fri, 29 Aug 2025 03:44:00 GMT  
		Size: 49.2 MB (49213158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc48901f36b0038823fc66a587782bcd79cd29b262bcdeb54ca8a5d8c38241e7`  
		Last Modified: Fri, 29 Aug 2025 03:43:57 GMT  
		Size: 1.7 MB (1712574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64fe4de3e909696bcb9189e0e6e5386374bc317fef0b4f298fc25104f773f5b`  
		Last Modified: Fri, 29 Aug 2025 03:43:57 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610d989a0365953e0828dcbe697cab36bb0360cbb7bc554bde86f42117518fac`  
		Last Modified: Fri, 29 Aug 2025 04:16:33 GMT  
		Size: 1.4 MB (1410318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf7402bf0405eabcf9ff96b07bf7f50c5a61dc63f676c13c6609f4a82130c6b`  
		Last Modified: Fri, 29 Aug 2025 04:16:33 GMT  
		Size: 11.7 MB (11665019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186feb277d2b3aa866a879927e6ac2a2f055558bb61e62904684010e741d9527`  
		Last Modified: Mon, 01 Sep 2025 22:38:46 GMT  
		Size: 122.9 MB (122867250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f77612ad47a3e7cd7d94544b5b7c12172342ba0a70ef19d3c58a9d99c93ff`  
		Last Modified: Mon, 01 Sep 2025 22:38:41 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6` - unknown; unknown

```console
$ docker pull ghost@sha256:41b9e9b1376b1deaa860ac578c75f1bfe6ba466b97f586953b697f8ba5b4e069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21555f60d49a223816f0075d68a3ee97aed16fcbfc27ed85677741c553ba158a`

```dockerfile
```

-	Layers:
	-	`sha256:613e5cad64b24765f0ee56b712968fe09103676d694c7a0020f2d505cd96504e`  
		Last Modified: Tue, 02 Sep 2025 00:46:02 GMT  
		Size: 5.5 MB (5525844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:035031bf928a9a4cef3690baf6c625f369d7203c6f88c38d7a19215607c48b96`  
		Last Modified: Tue, 02 Sep 2025 00:46:03 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6-alpine`

```console
$ docker pull ghost@sha256:241d70c34fa828eca8d66765bef9069101e4b7415cc66c8847189781a9476c9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:91f833eecc4992253bf2e13c105f86dc1159d5339bfc018ed5be16f72a493dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189158669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84682db32401f631317cfab0995a26deee1e10ed228f3c1eb8cc835773189111`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a088b2daae062d11086b47ecffca042d75b83c6228cb05d89c60c854c3265cd`  
		Last Modified: Thu, 28 Aug 2025 23:33:52 GMT  
		Size: 51.0 MB (51038593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52719e552fdfa1fbd5bd1e6ab184f77b28ec2b59509c98da3ef00ccb84385a51`  
		Last Modified: Thu, 28 Aug 2025 23:33:48 GMT  
		Size: 1.3 MB (1260576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016c0e95211121b6a80955630caaca8899d6572d51c48561f95a9ad97788a63a`  
		Last Modified: Thu, 28 Aug 2025 23:33:47 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de925af2263cc5733108b20f1307aadd37286544c6192f5cb716759071292d11`  
		Last Modified: Mon, 01 Sep 2025 22:31:51 GMT  
		Size: 777.0 KB (777044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8281e482037a7f2ad3b55f815b1991cb8736059ef8d0017f915ac77d88396ee2`  
		Last Modified: Mon, 01 Sep 2025 22:31:51 GMT  
		Size: 1.1 MB (1119680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ce3ee5e89722ee1206495e3b83765448a5e2a2ad539621912f11010081c79f`  
		Last Modified: Mon, 01 Sep 2025 22:31:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298d77339e9df897f9b2c3f379c0f0170b97e36ebf35ee6556c33fc473ffecb6`  
		Last Modified: Mon, 01 Sep 2025 22:31:52 GMT  
		Size: 11.6 MB (11649954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031f9f4d9480184dd899d41edd90d3a551e54b9cd72ddea2b99950cdae3edf5e`  
		Last Modified: Mon, 01 Sep 2025 22:32:08 GMT  
		Size: 119.5 MB (119511937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946901dca0fed560f284b1d5aa33c3ee1f708e5e0b372fd972c9e73fe3c6931f`  
		Last Modified: Mon, 01 Sep 2025 22:31:51 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:2090644e2273e294a1b163b6c6f41540d1d197615703cea04df60286da51f185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3353578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa275c6026465a55bc377f6facb26e86dcd47687dd707f66bbd9ca2d9edd789b`

```dockerfile
```

-	Layers:
	-	`sha256:75ac213a4fce41d283121567686347e62f02a0f965432531f28f2dc98a2878a5`  
		Last Modified: Tue, 02 Sep 2025 00:45:51 GMT  
		Size: 3.3 MB (3321018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2794d745c1764fec39ac34e2aa09421c2492d53fc296b7c8610efde123dc4a6`  
		Last Modified: Tue, 02 Sep 2025 00:45:52 GMT  
		Size: 32.6 KB (32560 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:2df270741ef2b8ff2bf4419a171aa1a63f0ff7602fb3ebb3c0e0e7583c371629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188005090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a94f7edfe8f77d4ebcf7e038c14a3d59c376d7abc45824069f224c34aa500b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2146ee5f8688ddaedbf432d5fdd81fdf801bc3702e1e4b1e88ccfe6742af7a85`  
		Last Modified: Fri, 29 Aug 2025 03:00:12 GMT  
		Size: 48.9 MB (48875724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a90f450bb70e1d8fb674b697d35665d29a8ff90d6889c7fd2eb35cb36605b9`  
		Last Modified: Fri, 29 Aug 2025 03:00:15 GMT  
		Size: 1.3 MB (1260558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c515feca2377d2626fa88b713494163a1cdff1171c103499951cd48af4b526`  
		Last Modified: Fri, 29 Aug 2025 03:00:17 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7ff7a2ec4d0e3047b7a7c53df837a2614e2888e24704026f2e384898b6ff5c`  
		Last Modified: Fri, 29 Aug 2025 03:18:13 GMT  
		Size: 766.1 KB (766090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4176a4ddf49558e4f9a77dceb3c7200d8f2141ecd342ba74f3efe31310731473`  
		Last Modified: Fri, 29 Aug 2025 03:18:13 GMT  
		Size: 1.1 MB (1086412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e2e78445aa3c6790af4ab280ae91842d700ccd3f154ff4776614a5eb10476e`  
		Last Modified: Fri, 29 Aug 2025 03:18:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a668c2aa22f30b84bc6fb72336e7d05a2650b67260fd1ca4e2045752fc7e6d`  
		Last Modified: Fri, 29 Aug 2025 03:18:15 GMT  
		Size: 11.6 MB (11641134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f60f74825c23e099c3ba3c72006a3763b5e14814c30f0adb88b5ad26c0c645`  
		Last Modified: Mon, 01 Sep 2025 22:36:56 GMT  
		Size: 120.9 MB (120873079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3c1ec5818d3312109d88fd1e3dfe43537b9e0a108357159f427cebeafc3538`  
		Last Modified: Mon, 01 Sep 2025 22:36:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c4b2dce4bf29921cedde2675784e7564e5618e20aebf587bf33d78852158d176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 KB (32473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c72f0d411e8410ce3acf99d574ecbc320ec7ddebf994ff20097f98ac9dd4c30`

```dockerfile
```

-	Layers:
	-	`sha256:1c3f1617c6df473c4b90ab5e39d5c2a6fe58cc334101d7c24e9cd01b12ba5a05`  
		Last Modified: Tue, 02 Sep 2025 00:45:56 GMT  
		Size: 32.5 KB (32473 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1d891cc1fb7d8e7c8dd6b11337dd72e5265da0aac33c3096c224d8011426a04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186696080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432fc1a614e658f0b1edf4dda8097ed0b7ae9deac05872975da47d7abac8e74d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a2ac9172cb928c21dfc13a44f44b5384646406904cbcf5cb5447f055a6faf`  
		Last Modified: Fri, 29 Aug 2025 02:40:14 GMT  
		Size: 48.2 MB (48205971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b346b9ed64232e8d2bf037abd74ba34428edf2022d9bfa4bad64bc663bee4afa`  
		Last Modified: Fri, 29 Aug 2025 02:40:09 GMT  
		Size: 1.3 MB (1260552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fce96b00aee190cd46335d78779e1b47369fe89758c84233632c09c72fca0a8`  
		Last Modified: Fri, 29 Aug 2025 02:40:09 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db594930f7577a6b22a63655fbaa30de582dcf6b9594e3d5285b1d62e3311ab`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 701.5 KB (701476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2096210d0c248b340441ad5727367aacda7d36b96a87fe37a9f35991277b2636`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 1.1 MB (1086412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e2384ad611ca10466ae91eade4ce3cade33bb653f6c94ccb92c82bd7528dce`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd553ef835b77c52adebbc84428e3e1ad25023b611483b6fb55f6499b6ea4a25`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 11.6 MB (11639252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e717a4dd3bdd4a20e0952069adf62e603539f8957181fcd65e1a6b73a2af39b3`  
		Last Modified: Mon, 01 Sep 2025 22:42:53 GMT  
		Size: 120.6 MB (120582192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667b1194461d829cefa3742b161e30635424106914d3edc32f671d327a8672d0`  
		Last Modified: Mon, 01 Sep 2025 22:42:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:244b91b2e350fca49aa385b9cd2e56a5486f97fd181b2db27495fa0558843429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3350731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791c2b8f0cb42980186a4beb8d0c61e0797425eab06eebd5e97dfa5d63a3a8e8`

```dockerfile
```

-	Layers:
	-	`sha256:ca6fad082a44e5495954aa768eac41d5b144f7de9b42467efdb6d7191bab4169`  
		Last Modified: Tue, 02 Sep 2025 00:46:00 GMT  
		Size: 3.3 MB (3318043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ce9bb40338deebe5eb758493429f77764f401f5d9e0c44d7fc0777815cfef9`  
		Last Modified: Tue, 02 Sep 2025 00:46:01 GMT  
		Size: 32.7 KB (32688 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0e6454198e858df07560da9e990be5cb4d051145059daff62fda9d3c572363bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 MB (199557367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec528d3e8439c0ba5bc9e05aa0783624295eb3ae9ea287cc99bdf31892d820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f45584a4c7a524e89b17213975d95dc9685cb0772da9368cb9c503770929cc`  
		Last Modified: Fri, 29 Aug 2025 01:25:44 GMT  
		Size: 50.3 MB (50301989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59516805c8635bd1d480d499042139bd7c135504095064ad26bb40302362ba61`  
		Last Modified: Fri, 29 Aug 2025 01:25:35 GMT  
		Size: 1.3 MB (1260576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0ef24f8fa23e77bc52551102b97ad4c00c4002412fd07b775bc3bf380ce272`  
		Last Modified: Fri, 29 Aug 2025 01:25:36 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1d4dd042ca3ee03655bd48d3301e60231319b4c9c9c985746ef53aaaa53fd9`  
		Last Modified: Fri, 29 Aug 2025 02:41:39 GMT  
		Size: 838.6 KB (838567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ec88dceaa42482ac7f2bad84002257eb8b6d56c65640a08a8ec003f5a99f89`  
		Last Modified: Fri, 29 Aug 2025 02:41:39 GMT  
		Size: 1.0 MB (1046735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61833974c4c0d23d6d38c884bbb5a8f926e832c46df98a7bbc8e23d2e909eecd`  
		Last Modified: Fri, 29 Aug 2025 02:41:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede081c9e5040427f30e26aeffdeabe4c80d51f9342a638603049878ba44552e`  
		Last Modified: Fri, 29 Aug 2025 02:41:41 GMT  
		Size: 11.7 MB (11650068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ce3cddce6ba7d99f36157a31d0cfe5694f17736ba959e6f7c20555ae66bf98`  
		Last Modified: Tue, 02 Sep 2025 00:45:58 GMT  
		Size: 130.3 MB (130327494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5080ffed4a8ebe32c590140e583d6ccf383301d98d3bfe02f03f7e9e82941fc2`  
		Last Modified: Mon, 01 Sep 2025 22:36:03 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:9e000df025b8c20aeb83dbd155e374734e17c99783bf3ff043e9c286c2cac7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3353849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb072d52e35d7a9ce8ff32a4e2ea0c2ba58f8f6b8f8c39be37fa0a54aa0328b4`

```dockerfile
```

-	Layers:
	-	`sha256:25a58b6f8d49541db4e4b56c4bb612094f3dfd1a17d606fb9fe9e3e77ef1e00e`  
		Last Modified: Tue, 02 Sep 2025 00:46:06 GMT  
		Size: 3.3 MB (3321126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3209e7af465e528a20ef16bb19b1e645c3653888e5f70f8250c7c60b693c82a`  
		Last Modified: Tue, 02 Sep 2025 00:46:07 GMT  
		Size: 32.7 KB (32723 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.0`

```console
$ docker pull ghost@sha256:2faf7cda2bfe29e925e30e14bed5250c6e326c7653a95e9358ff362717dc5b16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:6.0` - linux; amd64

```console
$ docker pull ghost@sha256:d2254b21222cfabdc215b43c92ac189c2351439a40ecdc83a41700f015f2b20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211763653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19035ba1f754fb7e686e3ead03ac05371fb6ebcb5a594235bb2c1c5cfcbd007d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291fc5dbbd39fe685232627c96a45e68110c8aa46cb7b065f3a72e72cb22c31d`  
		Last Modified: Thu, 28 Aug 2025 23:34:31 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2561d51a4c67aeb839775fbbf9f06e9b8f865499c3974f3b15d8748dcb0760a1`  
		Last Modified: Thu, 28 Aug 2025 23:34:37 GMT  
		Size: 49.0 MB (49010562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e06c1a47e17a8b62c4f581dfdec846741e13dbf17aacd62f8afa6d668d3da31`  
		Last Modified: Thu, 28 Aug 2025 23:34:30 GMT  
		Size: 1.7 MB (1712554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2403c8b76caca8d2d0a53ca1ee2475bbaece39b293a49cfba277b01186986bb8`  
		Last Modified: Thu, 28 Aug 2025 23:34:30 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76afcf2fa61fa51d34175604b2d563cce965bdb65b1c28ffb73a1ebc63e6336`  
		Last Modified: Mon, 01 Sep 2025 22:31:05 GMT  
		Size: 1.4 MB (1444945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799552c8963493fd20a6604b1b78f4ee50584bd1d896cc157402c8077ff42996`  
		Last Modified: Mon, 01 Sep 2025 22:31:09 GMT  
		Size: 11.7 MB (11650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c19a50e28a047b135e0e3ffe1247bfe04bd0fab6bac5514fc9af7d154ec8565`  
		Last Modified: Mon, 01 Sep 2025 22:31:12 GMT  
		Size: 119.7 MB (119710178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bc276376483c6b837fa4a33a535ec5c7d285e6d1bfabbfcfdcdecf51cb6f3a`  
		Last Modified: Mon, 01 Sep 2025 22:31:05 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0` - unknown; unknown

```console
$ docker pull ghost@sha256:b27a6f3720b8114a95d861609f204edb6ef9bd73fae96181e1a5dd45f9fb78e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a940a71b4fd4b3556eb01803ecb6e63b108795778c8545326b7c716c280201f7`

```dockerfile
```

-	Layers:
	-	`sha256:de464b26004e59cf977beb0f3cdaaff38e6b4f0833e766b1c0c2b047b89ab118`  
		Last Modified: Tue, 02 Sep 2025 00:45:38 GMT  
		Size: 5.5 MB (5532017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7237eef19ee9904fb66b59c2b8a3ea69d8f40436b916f5b639aeb4741b3a350b`  
		Last Modified: Tue, 02 Sep 2025 00:45:39 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.0` - linux; arm variant v7

```console
$ docker pull ghost@sha256:854fbd11e88160c51d9a2d06fe427d25c19c80cf285926b4fdd1bbecdc091f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203413730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd85aabdfbec73ec1790a771dee3d12061381067e87ad6b49b27cf1a6791172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae1e510a43ef8f416095b11f0182b2e280a16abb567ffe9973ee818f1ced070`  
		Last Modified: Wed, 13 Aug 2025 00:43:01 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5468eccc738adf70ee011b01680c456e47dc04f006dcce1b4cadbf6400263`  
		Last Modified: Fri, 29 Aug 2025 02:42:57 GMT  
		Size: 43.9 MB (43916785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb4b0ef6c2bf4f00b489a41c59c1355636508ad8cc8b009def82424800f2d4c`  
		Last Modified: Fri, 29 Aug 2025 02:42:50 GMT  
		Size: 1.7 MB (1712767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1951b39ccaea6be1c5650f48794d2610c4850f7643d2fbdecbabe1dbb6132054`  
		Last Modified: Fri, 29 Aug 2025 02:42:50 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17358ce1624416ef9ff445daec0c5f9d8b56d0dcf1ca981b81d3ad7fdfddfd0b`  
		Last Modified: Fri, 29 Aug 2025 03:47:51 GMT  
		Size: 1.4 MB (1412627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fb3436b4dbb0037988c989c6e85ea687ab350bd9981dbf00903c477c8bafd1`  
		Last Modified: Fri, 29 Aug 2025 03:47:52 GMT  
		Size: 11.6 MB (11639485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e3dae8a2aa6764159cd144d209389eff5907f4f61c783aaa231625e7a8d39d`  
		Last Modified: Mon, 01 Sep 2025 22:36:11 GMT  
		Size: 120.8 MB (120788809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad92ebadf2b39d220609d1b3753b850a1fff3f9a0944a8920801d6ec17ebb6c`  
		Last Modified: Mon, 01 Sep 2025 22:35:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0` - unknown; unknown

```console
$ docker pull ghost@sha256:9529ba666cb089cbee4321c0a853bbfea116482f0bfc39f0ea1d1f6cefdd5b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5564472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbd7cc01bc0a0f2f594146227aff39025b56fa682086132a547991bcd6afdbb`

```dockerfile
```

-	Layers:
	-	`sha256:bf14bc68813c966bbe8b2bf1ff2923aec3ecf68f0da115ce283156657960bc21`  
		Last Modified: Tue, 02 Sep 2025 00:45:44 GMT  
		Size: 5.5 MB (5534784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed46868ea90f3e5060df97e4ec073c47e70f770d42b0965956af5f8151ef7c0`  
		Last Modified: Tue, 02 Sep 2025 00:45:45 GMT  
		Size: 29.7 KB (29688 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.0` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:c71869bc85c04ac42db2d0206a23e0a0012e5dd2a6f3a8bad441bbadc3366b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211307491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d142eaca1b337deba2b831de051dfc274ac02c6088a19dfac39171a950b5f0c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27263372d67228bb86c6e522c8fc32c5e6a4a10ddabec215fa8026f3d01a3508`  
		Last Modified: Thu, 28 Aug 2025 14:40:51 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00ca1ce1c92f9f6153143bddfb381c493c0ae26d3bb85f10d228009ea618291`  
		Last Modified: Fri, 29 Aug 2025 01:27:40 GMT  
		Size: 48.7 MB (48681521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cceee3ed04b670a81910ab2d6400463c1c5253f81047942e7ca695dcbc42bef6`  
		Last Modified: Fri, 29 Aug 2025 01:27:34 GMT  
		Size: 1.7 MB (1712586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9a72dac5922748758980697ec36ffe4814be2e61e21f88b48746e419444192`  
		Last Modified: Fri, 29 Aug 2025 01:27:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990af4a1d6f18056eb115744e5360b959441c63cdac3679b104c29158bc34c5a`  
		Last Modified: Fri, 29 Aug 2025 03:09:43 GMT  
		Size: 1.4 MB (1376654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f35bbd74cc54bb41d37d13a7d299015b97e9b215c742395b169e75fab70ca9`  
		Last Modified: Fri, 29 Aug 2025 03:09:44 GMT  
		Size: 11.7 MB (11650392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918212475e1250b79cf2897198ed00dab67b0f619e097d00489a59f905971a9b`  
		Last Modified: Mon, 01 Sep 2025 22:30:55 GMT  
		Size: 119.8 MB (119800006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759453b512e79c73dbad92d0db51da292d1b4736fb10a248267fbaa032a39947`  
		Last Modified: Mon, 01 Sep 2025 22:30:46 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0` - unknown; unknown

```console
$ docker pull ghost@sha256:7ac6757f4114dc2990c62dd5793009785278c231ae38937c309497e88d36c4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f006d48f55bac7ca7915e12a9ca6c807b4d456d546d35e00b9b33e08cfb444a`

```dockerfile
```

-	Layers:
	-	`sha256:58e7d0eba6c644e7892aeecab188ec6b2e049a87cf4c7ba3cfbc24f721d37b4d`  
		Last Modified: Tue, 02 Sep 2025 00:45:50 GMT  
		Size: 5.5 MB (5532320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3aebc011dd0ca39b19da637deef8c255e64868975c603c86bd92ce8927eb314`  
		Last Modified: Tue, 02 Sep 2025 00:45:51 GMT  
		Size: 29.7 KB (29719 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.0` - linux; ppc64le

```console
$ docker pull ghost@sha256:684dad988bcc8867ee4f8dfa11a5310eaa7354dee2421b9b7713092f8ab66e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222396476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b174c7af12f48df75f029d34136182a00026b3cb584437bd99f6200273987d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db49890cc93d9412b095c6d9e7c7dcd1224e0b5c93c9c8848c12d48ecffbb89a`  
		Last Modified: Wed, 13 Aug 2025 13:16:33 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708047d400332a3ac027b4da8af825b8849d7cf6154f691f6b57c08995f18d5b`  
		Last Modified: Fri, 29 Aug 2025 00:58:52 GMT  
		Size: 51.9 MB (51930458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2905170ec9992e7f18c8d6a624109158fc4d528bbdc72a2bf3b6b5e54abeecd`  
		Last Modified: Fri, 29 Aug 2025 00:58:41 GMT  
		Size: 1.7 MB (1712753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa037f1a005a1ed7b76333d54b8874e5001c088200f60fdbf7a8bf41820a22b9`  
		Last Modified: Fri, 29 Aug 2025 00:58:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cca12707d80a0959f9c8c27d84527a6f395d044dbde84ed7dd6ac6581b59623`  
		Last Modified: Fri, 29 Aug 2025 02:23:49 GMT  
		Size: 1.4 MB (1366738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69098d5fc0ba8e36a59d67177ecb88d69fdec43caedb993f113cbe9548c40fb3`  
		Last Modified: Fri, 29 Aug 2025 02:23:51 GMT  
		Size: 11.7 MB (11650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad520b7406424dd17210f7bf38ab76bbe9e87b3d7c03bd5014dece708efcc6b`  
		Last Modified: Mon, 01 Sep 2025 22:38:59 GMT  
		Size: 123.7 MB (123658547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6c3733ec0f123b114febfe29247afaf79eddfd4d2dfef91760a3071c6eb2a6`  
		Last Modified: Mon, 01 Sep 2025 22:38:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0` - unknown; unknown

```console
$ docker pull ghost@sha256:c15a40d0d6240f38fbb67240a90432f06cca341a5b354a228eccd789c82f7e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c3c4216defb2246a1484c7c9923c2f4488015e3a0ca0c16da74179c1546e13`

```dockerfile
```

-	Layers:
	-	`sha256:55084258c84cba53b42a3dbd4c90b1e800fcfe8b5b1c6f943be6bfe1cf04681c`  
		Last Modified: Tue, 02 Sep 2025 00:45:56 GMT  
		Size: 5.5 MB (5531874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fc0054474cfcb15ca29acbded12e51e37f28f9ca1066504c1ff4dc22618766d`  
		Last Modified: Tue, 02 Sep 2025 00:45:57 GMT  
		Size: 29.6 KB (29634 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.0` - linux; s390x

```console
$ docker pull ghost@sha256:2fa624f4cf86e0d598710fd73c2f31b01ea41b83e7873a0ef079af1ecfc8a0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213760480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dcfcc37c5081780279297d15452f2a813e05bf8279e865fd109daa980d5b00b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dadfc3ada3cd4f49e71dc39867db6cf8d4c2cb806f817ea84710057fd1995b`  
		Last Modified: Wed, 13 Aug 2025 15:28:53 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3522eaaadd5604724d773f31f0376394ec59311b336e319267f643b81cd1051`  
		Last Modified: Fri, 29 Aug 2025 03:44:00 GMT  
		Size: 49.2 MB (49213158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc48901f36b0038823fc66a587782bcd79cd29b262bcdeb54ca8a5d8c38241e7`  
		Last Modified: Fri, 29 Aug 2025 03:43:57 GMT  
		Size: 1.7 MB (1712574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64fe4de3e909696bcb9189e0e6e5386374bc317fef0b4f298fc25104f773f5b`  
		Last Modified: Fri, 29 Aug 2025 03:43:57 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610d989a0365953e0828dcbe697cab36bb0360cbb7bc554bde86f42117518fac`  
		Last Modified: Fri, 29 Aug 2025 04:16:33 GMT  
		Size: 1.4 MB (1410318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf7402bf0405eabcf9ff96b07bf7f50c5a61dc63f676c13c6609f4a82130c6b`  
		Last Modified: Fri, 29 Aug 2025 04:16:33 GMT  
		Size: 11.7 MB (11665019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186feb277d2b3aa866a879927e6ac2a2f055558bb61e62904684010e741d9527`  
		Last Modified: Mon, 01 Sep 2025 22:38:46 GMT  
		Size: 122.9 MB (122867250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f77612ad47a3e7cd7d94544b5b7c12172342ba0a70ef19d3c58a9d99c93ff`  
		Last Modified: Mon, 01 Sep 2025 22:38:41 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0` - unknown; unknown

```console
$ docker pull ghost@sha256:41b9e9b1376b1deaa860ac578c75f1bfe6ba466b97f586953b697f8ba5b4e069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21555f60d49a223816f0075d68a3ee97aed16fcbfc27ed85677741c553ba158a`

```dockerfile
```

-	Layers:
	-	`sha256:613e5cad64b24765f0ee56b712968fe09103676d694c7a0020f2d505cd96504e`  
		Last Modified: Tue, 02 Sep 2025 00:46:02 GMT  
		Size: 5.5 MB (5525844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:035031bf928a9a4cef3690baf6c625f369d7203c6f88c38d7a19215607c48b96`  
		Last Modified: Tue, 02 Sep 2025 00:46:03 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.0-alpine`

```console
$ docker pull ghost@sha256:241d70c34fa828eca8d66765bef9069101e4b7415cc66c8847189781a9476c9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:91f833eecc4992253bf2e13c105f86dc1159d5339bfc018ed5be16f72a493dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189158669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84682db32401f631317cfab0995a26deee1e10ed228f3c1eb8cc835773189111`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a088b2daae062d11086b47ecffca042d75b83c6228cb05d89c60c854c3265cd`  
		Last Modified: Thu, 28 Aug 2025 23:33:52 GMT  
		Size: 51.0 MB (51038593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52719e552fdfa1fbd5bd1e6ab184f77b28ec2b59509c98da3ef00ccb84385a51`  
		Last Modified: Thu, 28 Aug 2025 23:33:48 GMT  
		Size: 1.3 MB (1260576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016c0e95211121b6a80955630caaca8899d6572d51c48561f95a9ad97788a63a`  
		Last Modified: Thu, 28 Aug 2025 23:33:47 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de925af2263cc5733108b20f1307aadd37286544c6192f5cb716759071292d11`  
		Last Modified: Mon, 01 Sep 2025 22:31:51 GMT  
		Size: 777.0 KB (777044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8281e482037a7f2ad3b55f815b1991cb8736059ef8d0017f915ac77d88396ee2`  
		Last Modified: Mon, 01 Sep 2025 22:31:51 GMT  
		Size: 1.1 MB (1119680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ce3ee5e89722ee1206495e3b83765448a5e2a2ad539621912f11010081c79f`  
		Last Modified: Mon, 01 Sep 2025 22:31:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298d77339e9df897f9b2c3f379c0f0170b97e36ebf35ee6556c33fc473ffecb6`  
		Last Modified: Mon, 01 Sep 2025 22:31:52 GMT  
		Size: 11.6 MB (11649954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031f9f4d9480184dd899d41edd90d3a551e54b9cd72ddea2b99950cdae3edf5e`  
		Last Modified: Mon, 01 Sep 2025 22:32:08 GMT  
		Size: 119.5 MB (119511937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946901dca0fed560f284b1d5aa33c3ee1f708e5e0b372fd972c9e73fe3c6931f`  
		Last Modified: Mon, 01 Sep 2025 22:31:51 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:2090644e2273e294a1b163b6c6f41540d1d197615703cea04df60286da51f185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3353578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa275c6026465a55bc377f6facb26e86dcd47687dd707f66bbd9ca2d9edd789b`

```dockerfile
```

-	Layers:
	-	`sha256:75ac213a4fce41d283121567686347e62f02a0f965432531f28f2dc98a2878a5`  
		Last Modified: Tue, 02 Sep 2025 00:45:51 GMT  
		Size: 3.3 MB (3321018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2794d745c1764fec39ac34e2aa09421c2492d53fc296b7c8610efde123dc4a6`  
		Last Modified: Tue, 02 Sep 2025 00:45:52 GMT  
		Size: 32.6 KB (32560 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.0-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:2df270741ef2b8ff2bf4419a171aa1a63f0ff7602fb3ebb3c0e0e7583c371629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188005090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a94f7edfe8f77d4ebcf7e038c14a3d59c376d7abc45824069f224c34aa500b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2146ee5f8688ddaedbf432d5fdd81fdf801bc3702e1e4b1e88ccfe6742af7a85`  
		Last Modified: Fri, 29 Aug 2025 03:00:12 GMT  
		Size: 48.9 MB (48875724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a90f450bb70e1d8fb674b697d35665d29a8ff90d6889c7fd2eb35cb36605b9`  
		Last Modified: Fri, 29 Aug 2025 03:00:15 GMT  
		Size: 1.3 MB (1260558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c515feca2377d2626fa88b713494163a1cdff1171c103499951cd48af4b526`  
		Last Modified: Fri, 29 Aug 2025 03:00:17 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7ff7a2ec4d0e3047b7a7c53df837a2614e2888e24704026f2e384898b6ff5c`  
		Last Modified: Fri, 29 Aug 2025 03:18:13 GMT  
		Size: 766.1 KB (766090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4176a4ddf49558e4f9a77dceb3c7200d8f2141ecd342ba74f3efe31310731473`  
		Last Modified: Fri, 29 Aug 2025 03:18:13 GMT  
		Size: 1.1 MB (1086412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e2e78445aa3c6790af4ab280ae91842d700ccd3f154ff4776614a5eb10476e`  
		Last Modified: Fri, 29 Aug 2025 03:18:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a668c2aa22f30b84bc6fb72336e7d05a2650b67260fd1ca4e2045752fc7e6d`  
		Last Modified: Fri, 29 Aug 2025 03:18:15 GMT  
		Size: 11.6 MB (11641134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f60f74825c23e099c3ba3c72006a3763b5e14814c30f0adb88b5ad26c0c645`  
		Last Modified: Mon, 01 Sep 2025 22:36:56 GMT  
		Size: 120.9 MB (120873079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3c1ec5818d3312109d88fd1e3dfe43537b9e0a108357159f427cebeafc3538`  
		Last Modified: Mon, 01 Sep 2025 22:36:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c4b2dce4bf29921cedde2675784e7564e5618e20aebf587bf33d78852158d176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 KB (32473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c72f0d411e8410ce3acf99d574ecbc320ec7ddebf994ff20097f98ac9dd4c30`

```dockerfile
```

-	Layers:
	-	`sha256:1c3f1617c6df473c4b90ab5e39d5c2a6fe58cc334101d7c24e9cd01b12ba5a05`  
		Last Modified: Tue, 02 Sep 2025 00:45:56 GMT  
		Size: 32.5 KB (32473 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.0-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1d891cc1fb7d8e7c8dd6b11337dd72e5265da0aac33c3096c224d8011426a04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186696080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432fc1a614e658f0b1edf4dda8097ed0b7ae9deac05872975da47d7abac8e74d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a2ac9172cb928c21dfc13a44f44b5384646406904cbcf5cb5447f055a6faf`  
		Last Modified: Fri, 29 Aug 2025 02:40:14 GMT  
		Size: 48.2 MB (48205971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b346b9ed64232e8d2bf037abd74ba34428edf2022d9bfa4bad64bc663bee4afa`  
		Last Modified: Fri, 29 Aug 2025 02:40:09 GMT  
		Size: 1.3 MB (1260552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fce96b00aee190cd46335d78779e1b47369fe89758c84233632c09c72fca0a8`  
		Last Modified: Fri, 29 Aug 2025 02:40:09 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db594930f7577a6b22a63655fbaa30de582dcf6b9594e3d5285b1d62e3311ab`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 701.5 KB (701476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2096210d0c248b340441ad5727367aacda7d36b96a87fe37a9f35991277b2636`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 1.1 MB (1086412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e2384ad611ca10466ae91eade4ce3cade33bb653f6c94ccb92c82bd7528dce`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd553ef835b77c52adebbc84428e3e1ad25023b611483b6fb55f6499b6ea4a25`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 11.6 MB (11639252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e717a4dd3bdd4a20e0952069adf62e603539f8957181fcd65e1a6b73a2af39b3`  
		Last Modified: Mon, 01 Sep 2025 22:42:53 GMT  
		Size: 120.6 MB (120582192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667b1194461d829cefa3742b161e30635424106914d3edc32f671d327a8672d0`  
		Last Modified: Mon, 01 Sep 2025 22:42:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:244b91b2e350fca49aa385b9cd2e56a5486f97fd181b2db27495fa0558843429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3350731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791c2b8f0cb42980186a4beb8d0c61e0797425eab06eebd5e97dfa5d63a3a8e8`

```dockerfile
```

-	Layers:
	-	`sha256:ca6fad082a44e5495954aa768eac41d5b144f7de9b42467efdb6d7191bab4169`  
		Last Modified: Tue, 02 Sep 2025 00:46:00 GMT  
		Size: 3.3 MB (3318043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ce9bb40338deebe5eb758493429f77764f401f5d9e0c44d7fc0777815cfef9`  
		Last Modified: Tue, 02 Sep 2025 00:46:01 GMT  
		Size: 32.7 KB (32688 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.0-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0e6454198e858df07560da9e990be5cb4d051145059daff62fda9d3c572363bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 MB (199557367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec528d3e8439c0ba5bc9e05aa0783624295eb3ae9ea287cc99bdf31892d820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f45584a4c7a524e89b17213975d95dc9685cb0772da9368cb9c503770929cc`  
		Last Modified: Fri, 29 Aug 2025 01:25:44 GMT  
		Size: 50.3 MB (50301989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59516805c8635bd1d480d499042139bd7c135504095064ad26bb40302362ba61`  
		Last Modified: Fri, 29 Aug 2025 01:25:35 GMT  
		Size: 1.3 MB (1260576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0ef24f8fa23e77bc52551102b97ad4c00c4002412fd07b775bc3bf380ce272`  
		Last Modified: Fri, 29 Aug 2025 01:25:36 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1d4dd042ca3ee03655bd48d3301e60231319b4c9c9c985746ef53aaaa53fd9`  
		Last Modified: Fri, 29 Aug 2025 02:41:39 GMT  
		Size: 838.6 KB (838567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ec88dceaa42482ac7f2bad84002257eb8b6d56c65640a08a8ec003f5a99f89`  
		Last Modified: Fri, 29 Aug 2025 02:41:39 GMT  
		Size: 1.0 MB (1046735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61833974c4c0d23d6d38c884bbb5a8f926e832c46df98a7bbc8e23d2e909eecd`  
		Last Modified: Fri, 29 Aug 2025 02:41:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede081c9e5040427f30e26aeffdeabe4c80d51f9342a638603049878ba44552e`  
		Last Modified: Fri, 29 Aug 2025 02:41:41 GMT  
		Size: 11.7 MB (11650068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ce3cddce6ba7d99f36157a31d0cfe5694f17736ba959e6f7c20555ae66bf98`  
		Last Modified: Tue, 02 Sep 2025 00:45:58 GMT  
		Size: 130.3 MB (130327494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5080ffed4a8ebe32c590140e583d6ccf383301d98d3bfe02f03f7e9e82941fc2`  
		Last Modified: Mon, 01 Sep 2025 22:36:03 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:9e000df025b8c20aeb83dbd155e374734e17c99783bf3ff043e9c286c2cac7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3353849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb072d52e35d7a9ce8ff32a4e2ea0c2ba58f8f6b8f8c39be37fa0a54aa0328b4`

```dockerfile
```

-	Layers:
	-	`sha256:25a58b6f8d49541db4e4b56c4bb612094f3dfd1a17d606fb9fe9e3e77ef1e00e`  
		Last Modified: Tue, 02 Sep 2025 00:46:06 GMT  
		Size: 3.3 MB (3321126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3209e7af465e528a20ef16bb19b1e645c3653888e5f70f8250c7c60b693c82a`  
		Last Modified: Tue, 02 Sep 2025 00:46:07 GMT  
		Size: 32.7 KB (32723 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.0.6`

```console
$ docker pull ghost@sha256:2faf7cda2bfe29e925e30e14bed5250c6e326c7653a95e9358ff362717dc5b16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:6.0.6` - linux; amd64

```console
$ docker pull ghost@sha256:d2254b21222cfabdc215b43c92ac189c2351439a40ecdc83a41700f015f2b20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211763653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19035ba1f754fb7e686e3ead03ac05371fb6ebcb5a594235bb2c1c5cfcbd007d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291fc5dbbd39fe685232627c96a45e68110c8aa46cb7b065f3a72e72cb22c31d`  
		Last Modified: Thu, 28 Aug 2025 23:34:31 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2561d51a4c67aeb839775fbbf9f06e9b8f865499c3974f3b15d8748dcb0760a1`  
		Last Modified: Thu, 28 Aug 2025 23:34:37 GMT  
		Size: 49.0 MB (49010562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e06c1a47e17a8b62c4f581dfdec846741e13dbf17aacd62f8afa6d668d3da31`  
		Last Modified: Thu, 28 Aug 2025 23:34:30 GMT  
		Size: 1.7 MB (1712554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2403c8b76caca8d2d0a53ca1ee2475bbaece39b293a49cfba277b01186986bb8`  
		Last Modified: Thu, 28 Aug 2025 23:34:30 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76afcf2fa61fa51d34175604b2d563cce965bdb65b1c28ffb73a1ebc63e6336`  
		Last Modified: Mon, 01 Sep 2025 22:31:05 GMT  
		Size: 1.4 MB (1444945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799552c8963493fd20a6604b1b78f4ee50584bd1d896cc157402c8077ff42996`  
		Last Modified: Mon, 01 Sep 2025 22:31:09 GMT  
		Size: 11.7 MB (11650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c19a50e28a047b135e0e3ffe1247bfe04bd0fab6bac5514fc9af7d154ec8565`  
		Last Modified: Mon, 01 Sep 2025 22:31:12 GMT  
		Size: 119.7 MB (119710178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bc276376483c6b837fa4a33a535ec5c7d285e6d1bfabbfcfdcdecf51cb6f3a`  
		Last Modified: Mon, 01 Sep 2025 22:31:05 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0.6` - unknown; unknown

```console
$ docker pull ghost@sha256:b27a6f3720b8114a95d861609f204edb6ef9bd73fae96181e1a5dd45f9fb78e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a940a71b4fd4b3556eb01803ecb6e63b108795778c8545326b7c716c280201f7`

```dockerfile
```

-	Layers:
	-	`sha256:de464b26004e59cf977beb0f3cdaaff38e6b4f0833e766b1c0c2b047b89ab118`  
		Last Modified: Tue, 02 Sep 2025 00:45:38 GMT  
		Size: 5.5 MB (5532017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7237eef19ee9904fb66b59c2b8a3ea69d8f40436b916f5b639aeb4741b3a350b`  
		Last Modified: Tue, 02 Sep 2025 00:45:39 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.0.6` - linux; arm variant v7

```console
$ docker pull ghost@sha256:854fbd11e88160c51d9a2d06fe427d25c19c80cf285926b4fdd1bbecdc091f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203413730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd85aabdfbec73ec1790a771dee3d12061381067e87ad6b49b27cf1a6791172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae1e510a43ef8f416095b11f0182b2e280a16abb567ffe9973ee818f1ced070`  
		Last Modified: Wed, 13 Aug 2025 00:43:01 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5468eccc738adf70ee011b01680c456e47dc04f006dcce1b4cadbf6400263`  
		Last Modified: Fri, 29 Aug 2025 02:42:57 GMT  
		Size: 43.9 MB (43916785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb4b0ef6c2bf4f00b489a41c59c1355636508ad8cc8b009def82424800f2d4c`  
		Last Modified: Fri, 29 Aug 2025 02:42:50 GMT  
		Size: 1.7 MB (1712767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1951b39ccaea6be1c5650f48794d2610c4850f7643d2fbdecbabe1dbb6132054`  
		Last Modified: Fri, 29 Aug 2025 02:42:50 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17358ce1624416ef9ff445daec0c5f9d8b56d0dcf1ca981b81d3ad7fdfddfd0b`  
		Last Modified: Fri, 29 Aug 2025 03:47:51 GMT  
		Size: 1.4 MB (1412627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fb3436b4dbb0037988c989c6e85ea687ab350bd9981dbf00903c477c8bafd1`  
		Last Modified: Fri, 29 Aug 2025 03:47:52 GMT  
		Size: 11.6 MB (11639485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e3dae8a2aa6764159cd144d209389eff5907f4f61c783aaa231625e7a8d39d`  
		Last Modified: Mon, 01 Sep 2025 22:36:11 GMT  
		Size: 120.8 MB (120788809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad92ebadf2b39d220609d1b3753b850a1fff3f9a0944a8920801d6ec17ebb6c`  
		Last Modified: Mon, 01 Sep 2025 22:35:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0.6` - unknown; unknown

```console
$ docker pull ghost@sha256:9529ba666cb089cbee4321c0a853bbfea116482f0bfc39f0ea1d1f6cefdd5b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5564472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbd7cc01bc0a0f2f594146227aff39025b56fa682086132a547991bcd6afdbb`

```dockerfile
```

-	Layers:
	-	`sha256:bf14bc68813c966bbe8b2bf1ff2923aec3ecf68f0da115ce283156657960bc21`  
		Last Modified: Tue, 02 Sep 2025 00:45:44 GMT  
		Size: 5.5 MB (5534784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed46868ea90f3e5060df97e4ec073c47e70f770d42b0965956af5f8151ef7c0`  
		Last Modified: Tue, 02 Sep 2025 00:45:45 GMT  
		Size: 29.7 KB (29688 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.0.6` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:c71869bc85c04ac42db2d0206a23e0a0012e5dd2a6f3a8bad441bbadc3366b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211307491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d142eaca1b337deba2b831de051dfc274ac02c6088a19dfac39171a950b5f0c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27263372d67228bb86c6e522c8fc32c5e6a4a10ddabec215fa8026f3d01a3508`  
		Last Modified: Thu, 28 Aug 2025 14:40:51 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00ca1ce1c92f9f6153143bddfb381c493c0ae26d3bb85f10d228009ea618291`  
		Last Modified: Fri, 29 Aug 2025 01:27:40 GMT  
		Size: 48.7 MB (48681521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cceee3ed04b670a81910ab2d6400463c1c5253f81047942e7ca695dcbc42bef6`  
		Last Modified: Fri, 29 Aug 2025 01:27:34 GMT  
		Size: 1.7 MB (1712586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9a72dac5922748758980697ec36ffe4814be2e61e21f88b48746e419444192`  
		Last Modified: Fri, 29 Aug 2025 01:27:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990af4a1d6f18056eb115744e5360b959441c63cdac3679b104c29158bc34c5a`  
		Last Modified: Fri, 29 Aug 2025 03:09:43 GMT  
		Size: 1.4 MB (1376654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f35bbd74cc54bb41d37d13a7d299015b97e9b215c742395b169e75fab70ca9`  
		Last Modified: Fri, 29 Aug 2025 03:09:44 GMT  
		Size: 11.7 MB (11650392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918212475e1250b79cf2897198ed00dab67b0f619e097d00489a59f905971a9b`  
		Last Modified: Mon, 01 Sep 2025 22:30:55 GMT  
		Size: 119.8 MB (119800006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759453b512e79c73dbad92d0db51da292d1b4736fb10a248267fbaa032a39947`  
		Last Modified: Mon, 01 Sep 2025 22:30:46 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0.6` - unknown; unknown

```console
$ docker pull ghost@sha256:7ac6757f4114dc2990c62dd5793009785278c231ae38937c309497e88d36c4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f006d48f55bac7ca7915e12a9ca6c807b4d456d546d35e00b9b33e08cfb444a`

```dockerfile
```

-	Layers:
	-	`sha256:58e7d0eba6c644e7892aeecab188ec6b2e049a87cf4c7ba3cfbc24f721d37b4d`  
		Last Modified: Tue, 02 Sep 2025 00:45:50 GMT  
		Size: 5.5 MB (5532320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3aebc011dd0ca39b19da637deef8c255e64868975c603c86bd92ce8927eb314`  
		Last Modified: Tue, 02 Sep 2025 00:45:51 GMT  
		Size: 29.7 KB (29719 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.0.6` - linux; ppc64le

```console
$ docker pull ghost@sha256:684dad988bcc8867ee4f8dfa11a5310eaa7354dee2421b9b7713092f8ab66e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222396476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b174c7af12f48df75f029d34136182a00026b3cb584437bd99f6200273987d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db49890cc93d9412b095c6d9e7c7dcd1224e0b5c93c9c8848c12d48ecffbb89a`  
		Last Modified: Wed, 13 Aug 2025 13:16:33 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708047d400332a3ac027b4da8af825b8849d7cf6154f691f6b57c08995f18d5b`  
		Last Modified: Fri, 29 Aug 2025 00:58:52 GMT  
		Size: 51.9 MB (51930458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2905170ec9992e7f18c8d6a624109158fc4d528bbdc72a2bf3b6b5e54abeecd`  
		Last Modified: Fri, 29 Aug 2025 00:58:41 GMT  
		Size: 1.7 MB (1712753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa037f1a005a1ed7b76333d54b8874e5001c088200f60fdbf7a8bf41820a22b9`  
		Last Modified: Fri, 29 Aug 2025 00:58:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cca12707d80a0959f9c8c27d84527a6f395d044dbde84ed7dd6ac6581b59623`  
		Last Modified: Fri, 29 Aug 2025 02:23:49 GMT  
		Size: 1.4 MB (1366738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69098d5fc0ba8e36a59d67177ecb88d69fdec43caedb993f113cbe9548c40fb3`  
		Last Modified: Fri, 29 Aug 2025 02:23:51 GMT  
		Size: 11.7 MB (11650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad520b7406424dd17210f7bf38ab76bbe9e87b3d7c03bd5014dece708efcc6b`  
		Last Modified: Mon, 01 Sep 2025 22:38:59 GMT  
		Size: 123.7 MB (123658547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6c3733ec0f123b114febfe29247afaf79eddfd4d2dfef91760a3071c6eb2a6`  
		Last Modified: Mon, 01 Sep 2025 22:38:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0.6` - unknown; unknown

```console
$ docker pull ghost@sha256:c15a40d0d6240f38fbb67240a90432f06cca341a5b354a228eccd789c82f7e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c3c4216defb2246a1484c7c9923c2f4488015e3a0ca0c16da74179c1546e13`

```dockerfile
```

-	Layers:
	-	`sha256:55084258c84cba53b42a3dbd4c90b1e800fcfe8b5b1c6f943be6bfe1cf04681c`  
		Last Modified: Tue, 02 Sep 2025 00:45:56 GMT  
		Size: 5.5 MB (5531874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fc0054474cfcb15ca29acbded12e51e37f28f9ca1066504c1ff4dc22618766d`  
		Last Modified: Tue, 02 Sep 2025 00:45:57 GMT  
		Size: 29.6 KB (29634 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.0.6` - linux; s390x

```console
$ docker pull ghost@sha256:2fa624f4cf86e0d598710fd73c2f31b01ea41b83e7873a0ef079af1ecfc8a0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213760480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dcfcc37c5081780279297d15452f2a813e05bf8279e865fd109daa980d5b00b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dadfc3ada3cd4f49e71dc39867db6cf8d4c2cb806f817ea84710057fd1995b`  
		Last Modified: Wed, 13 Aug 2025 15:28:53 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3522eaaadd5604724d773f31f0376394ec59311b336e319267f643b81cd1051`  
		Last Modified: Fri, 29 Aug 2025 03:44:00 GMT  
		Size: 49.2 MB (49213158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc48901f36b0038823fc66a587782bcd79cd29b262bcdeb54ca8a5d8c38241e7`  
		Last Modified: Fri, 29 Aug 2025 03:43:57 GMT  
		Size: 1.7 MB (1712574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64fe4de3e909696bcb9189e0e6e5386374bc317fef0b4f298fc25104f773f5b`  
		Last Modified: Fri, 29 Aug 2025 03:43:57 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610d989a0365953e0828dcbe697cab36bb0360cbb7bc554bde86f42117518fac`  
		Last Modified: Fri, 29 Aug 2025 04:16:33 GMT  
		Size: 1.4 MB (1410318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf7402bf0405eabcf9ff96b07bf7f50c5a61dc63f676c13c6609f4a82130c6b`  
		Last Modified: Fri, 29 Aug 2025 04:16:33 GMT  
		Size: 11.7 MB (11665019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186feb277d2b3aa866a879927e6ac2a2f055558bb61e62904684010e741d9527`  
		Last Modified: Mon, 01 Sep 2025 22:38:46 GMT  
		Size: 122.9 MB (122867250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f77612ad47a3e7cd7d94544b5b7c12172342ba0a70ef19d3c58a9d99c93ff`  
		Last Modified: Mon, 01 Sep 2025 22:38:41 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0.6` - unknown; unknown

```console
$ docker pull ghost@sha256:41b9e9b1376b1deaa860ac578c75f1bfe6ba466b97f586953b697f8ba5b4e069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21555f60d49a223816f0075d68a3ee97aed16fcbfc27ed85677741c553ba158a`

```dockerfile
```

-	Layers:
	-	`sha256:613e5cad64b24765f0ee56b712968fe09103676d694c7a0020f2d505cd96504e`  
		Last Modified: Tue, 02 Sep 2025 00:46:02 GMT  
		Size: 5.5 MB (5525844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:035031bf928a9a4cef3690baf6c625f369d7203c6f88c38d7a19215607c48b96`  
		Last Modified: Tue, 02 Sep 2025 00:46:03 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:6.0.6-alpine`

```console
$ docker pull ghost@sha256:241d70c34fa828eca8d66765bef9069101e4b7415cc66c8847189781a9476c9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:6.0.6-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:91f833eecc4992253bf2e13c105f86dc1159d5339bfc018ed5be16f72a493dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189158669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84682db32401f631317cfab0995a26deee1e10ed228f3c1eb8cc835773189111`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a088b2daae062d11086b47ecffca042d75b83c6228cb05d89c60c854c3265cd`  
		Last Modified: Thu, 28 Aug 2025 23:33:52 GMT  
		Size: 51.0 MB (51038593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52719e552fdfa1fbd5bd1e6ab184f77b28ec2b59509c98da3ef00ccb84385a51`  
		Last Modified: Thu, 28 Aug 2025 23:33:48 GMT  
		Size: 1.3 MB (1260576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016c0e95211121b6a80955630caaca8899d6572d51c48561f95a9ad97788a63a`  
		Last Modified: Thu, 28 Aug 2025 23:33:47 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de925af2263cc5733108b20f1307aadd37286544c6192f5cb716759071292d11`  
		Last Modified: Mon, 01 Sep 2025 22:31:51 GMT  
		Size: 777.0 KB (777044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8281e482037a7f2ad3b55f815b1991cb8736059ef8d0017f915ac77d88396ee2`  
		Last Modified: Mon, 01 Sep 2025 22:31:51 GMT  
		Size: 1.1 MB (1119680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ce3ee5e89722ee1206495e3b83765448a5e2a2ad539621912f11010081c79f`  
		Last Modified: Mon, 01 Sep 2025 22:31:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298d77339e9df897f9b2c3f379c0f0170b97e36ebf35ee6556c33fc473ffecb6`  
		Last Modified: Mon, 01 Sep 2025 22:31:52 GMT  
		Size: 11.6 MB (11649954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031f9f4d9480184dd899d41edd90d3a551e54b9cd72ddea2b99950cdae3edf5e`  
		Last Modified: Mon, 01 Sep 2025 22:32:08 GMT  
		Size: 119.5 MB (119511937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946901dca0fed560f284b1d5aa33c3ee1f708e5e0b372fd972c9e73fe3c6931f`  
		Last Modified: Mon, 01 Sep 2025 22:31:51 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0.6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:2090644e2273e294a1b163b6c6f41540d1d197615703cea04df60286da51f185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3353578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa275c6026465a55bc377f6facb26e86dcd47687dd707f66bbd9ca2d9edd789b`

```dockerfile
```

-	Layers:
	-	`sha256:75ac213a4fce41d283121567686347e62f02a0f965432531f28f2dc98a2878a5`  
		Last Modified: Tue, 02 Sep 2025 00:45:51 GMT  
		Size: 3.3 MB (3321018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2794d745c1764fec39ac34e2aa09421c2492d53fc296b7c8610efde123dc4a6`  
		Last Modified: Tue, 02 Sep 2025 00:45:52 GMT  
		Size: 32.6 KB (32560 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.0.6-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:2df270741ef2b8ff2bf4419a171aa1a63f0ff7602fb3ebb3c0e0e7583c371629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188005090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a94f7edfe8f77d4ebcf7e038c14a3d59c376d7abc45824069f224c34aa500b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2146ee5f8688ddaedbf432d5fdd81fdf801bc3702e1e4b1e88ccfe6742af7a85`  
		Last Modified: Fri, 29 Aug 2025 03:00:12 GMT  
		Size: 48.9 MB (48875724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a90f450bb70e1d8fb674b697d35665d29a8ff90d6889c7fd2eb35cb36605b9`  
		Last Modified: Fri, 29 Aug 2025 03:00:15 GMT  
		Size: 1.3 MB (1260558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c515feca2377d2626fa88b713494163a1cdff1171c103499951cd48af4b526`  
		Last Modified: Fri, 29 Aug 2025 03:00:17 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7ff7a2ec4d0e3047b7a7c53df837a2614e2888e24704026f2e384898b6ff5c`  
		Last Modified: Fri, 29 Aug 2025 03:18:13 GMT  
		Size: 766.1 KB (766090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4176a4ddf49558e4f9a77dceb3c7200d8f2141ecd342ba74f3efe31310731473`  
		Last Modified: Fri, 29 Aug 2025 03:18:13 GMT  
		Size: 1.1 MB (1086412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e2e78445aa3c6790af4ab280ae91842d700ccd3f154ff4776614a5eb10476e`  
		Last Modified: Fri, 29 Aug 2025 03:18:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a668c2aa22f30b84bc6fb72336e7d05a2650b67260fd1ca4e2045752fc7e6d`  
		Last Modified: Fri, 29 Aug 2025 03:18:15 GMT  
		Size: 11.6 MB (11641134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f60f74825c23e099c3ba3c72006a3763b5e14814c30f0adb88b5ad26c0c645`  
		Last Modified: Mon, 01 Sep 2025 22:36:56 GMT  
		Size: 120.9 MB (120873079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3c1ec5818d3312109d88fd1e3dfe43537b9e0a108357159f427cebeafc3538`  
		Last Modified: Mon, 01 Sep 2025 22:36:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0.6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c4b2dce4bf29921cedde2675784e7564e5618e20aebf587bf33d78852158d176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 KB (32473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c72f0d411e8410ce3acf99d574ecbc320ec7ddebf994ff20097f98ac9dd4c30`

```dockerfile
```

-	Layers:
	-	`sha256:1c3f1617c6df473c4b90ab5e39d5c2a6fe58cc334101d7c24e9cd01b12ba5a05`  
		Last Modified: Tue, 02 Sep 2025 00:45:56 GMT  
		Size: 32.5 KB (32473 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.0.6-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1d891cc1fb7d8e7c8dd6b11337dd72e5265da0aac33c3096c224d8011426a04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186696080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432fc1a614e658f0b1edf4dda8097ed0b7ae9deac05872975da47d7abac8e74d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a2ac9172cb928c21dfc13a44f44b5384646406904cbcf5cb5447f055a6faf`  
		Last Modified: Fri, 29 Aug 2025 02:40:14 GMT  
		Size: 48.2 MB (48205971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b346b9ed64232e8d2bf037abd74ba34428edf2022d9bfa4bad64bc663bee4afa`  
		Last Modified: Fri, 29 Aug 2025 02:40:09 GMT  
		Size: 1.3 MB (1260552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fce96b00aee190cd46335d78779e1b47369fe89758c84233632c09c72fca0a8`  
		Last Modified: Fri, 29 Aug 2025 02:40:09 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db594930f7577a6b22a63655fbaa30de582dcf6b9594e3d5285b1d62e3311ab`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 701.5 KB (701476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2096210d0c248b340441ad5727367aacda7d36b96a87fe37a9f35991277b2636`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 1.1 MB (1086412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e2384ad611ca10466ae91eade4ce3cade33bb653f6c94ccb92c82bd7528dce`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd553ef835b77c52adebbc84428e3e1ad25023b611483b6fb55f6499b6ea4a25`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 11.6 MB (11639252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e717a4dd3bdd4a20e0952069adf62e603539f8957181fcd65e1a6b73a2af39b3`  
		Last Modified: Mon, 01 Sep 2025 22:42:53 GMT  
		Size: 120.6 MB (120582192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667b1194461d829cefa3742b161e30635424106914d3edc32f671d327a8672d0`  
		Last Modified: Mon, 01 Sep 2025 22:42:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0.6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:244b91b2e350fca49aa385b9cd2e56a5486f97fd181b2db27495fa0558843429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3350731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791c2b8f0cb42980186a4beb8d0c61e0797425eab06eebd5e97dfa5d63a3a8e8`

```dockerfile
```

-	Layers:
	-	`sha256:ca6fad082a44e5495954aa768eac41d5b144f7de9b42467efdb6d7191bab4169`  
		Last Modified: Tue, 02 Sep 2025 00:46:00 GMT  
		Size: 3.3 MB (3318043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ce9bb40338deebe5eb758493429f77764f401f5d9e0c44d7fc0777815cfef9`  
		Last Modified: Tue, 02 Sep 2025 00:46:01 GMT  
		Size: 32.7 KB (32688 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:6.0.6-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0e6454198e858df07560da9e990be5cb4d051145059daff62fda9d3c572363bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 MB (199557367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec528d3e8439c0ba5bc9e05aa0783624295eb3ae9ea287cc99bdf31892d820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f45584a4c7a524e89b17213975d95dc9685cb0772da9368cb9c503770929cc`  
		Last Modified: Fri, 29 Aug 2025 01:25:44 GMT  
		Size: 50.3 MB (50301989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59516805c8635bd1d480d499042139bd7c135504095064ad26bb40302362ba61`  
		Last Modified: Fri, 29 Aug 2025 01:25:35 GMT  
		Size: 1.3 MB (1260576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0ef24f8fa23e77bc52551102b97ad4c00c4002412fd07b775bc3bf380ce272`  
		Last Modified: Fri, 29 Aug 2025 01:25:36 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1d4dd042ca3ee03655bd48d3301e60231319b4c9c9c985746ef53aaaa53fd9`  
		Last Modified: Fri, 29 Aug 2025 02:41:39 GMT  
		Size: 838.6 KB (838567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ec88dceaa42482ac7f2bad84002257eb8b6d56c65640a08a8ec003f5a99f89`  
		Last Modified: Fri, 29 Aug 2025 02:41:39 GMT  
		Size: 1.0 MB (1046735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61833974c4c0d23d6d38c884bbb5a8f926e832c46df98a7bbc8e23d2e909eecd`  
		Last Modified: Fri, 29 Aug 2025 02:41:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede081c9e5040427f30e26aeffdeabe4c80d51f9342a638603049878ba44552e`  
		Last Modified: Fri, 29 Aug 2025 02:41:41 GMT  
		Size: 11.7 MB (11650068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ce3cddce6ba7d99f36157a31d0cfe5694f17736ba959e6f7c20555ae66bf98`  
		Last Modified: Tue, 02 Sep 2025 00:45:58 GMT  
		Size: 130.3 MB (130327494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5080ffed4a8ebe32c590140e583d6ccf383301d98d3bfe02f03f7e9e82941fc2`  
		Last Modified: Mon, 01 Sep 2025 22:36:03 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:6.0.6-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:9e000df025b8c20aeb83dbd155e374734e17c99783bf3ff043e9c286c2cac7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3353849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb072d52e35d7a9ce8ff32a4e2ea0c2ba58f8f6b8f8c39be37fa0a54aa0328b4`

```dockerfile
```

-	Layers:
	-	`sha256:25a58b6f8d49541db4e4b56c4bb612094f3dfd1a17d606fb9fe9e3e77ef1e00e`  
		Last Modified: Tue, 02 Sep 2025 00:46:06 GMT  
		Size: 3.3 MB (3321126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3209e7af465e528a20ef16bb19b1e645c3653888e5f70f8250c7c60b693c82a`  
		Last Modified: Tue, 02 Sep 2025 00:46:07 GMT  
		Size: 32.7 KB (32723 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:alpine`

```console
$ docker pull ghost@sha256:241d70c34fa828eca8d66765bef9069101e4b7415cc66c8847189781a9476c9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:91f833eecc4992253bf2e13c105f86dc1159d5339bfc018ed5be16f72a493dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189158669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84682db32401f631317cfab0995a26deee1e10ed228f3c1eb8cc835773189111`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a088b2daae062d11086b47ecffca042d75b83c6228cb05d89c60c854c3265cd`  
		Last Modified: Thu, 28 Aug 2025 23:33:52 GMT  
		Size: 51.0 MB (51038593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52719e552fdfa1fbd5bd1e6ab184f77b28ec2b59509c98da3ef00ccb84385a51`  
		Last Modified: Thu, 28 Aug 2025 23:33:48 GMT  
		Size: 1.3 MB (1260576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016c0e95211121b6a80955630caaca8899d6572d51c48561f95a9ad97788a63a`  
		Last Modified: Thu, 28 Aug 2025 23:33:47 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de925af2263cc5733108b20f1307aadd37286544c6192f5cb716759071292d11`  
		Last Modified: Mon, 01 Sep 2025 22:31:51 GMT  
		Size: 777.0 KB (777044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8281e482037a7f2ad3b55f815b1991cb8736059ef8d0017f915ac77d88396ee2`  
		Last Modified: Mon, 01 Sep 2025 22:31:51 GMT  
		Size: 1.1 MB (1119680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ce3ee5e89722ee1206495e3b83765448a5e2a2ad539621912f11010081c79f`  
		Last Modified: Mon, 01 Sep 2025 22:31:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298d77339e9df897f9b2c3f379c0f0170b97e36ebf35ee6556c33fc473ffecb6`  
		Last Modified: Mon, 01 Sep 2025 22:31:52 GMT  
		Size: 11.6 MB (11649954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031f9f4d9480184dd899d41edd90d3a551e54b9cd72ddea2b99950cdae3edf5e`  
		Last Modified: Mon, 01 Sep 2025 22:32:08 GMT  
		Size: 119.5 MB (119511937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946901dca0fed560f284b1d5aa33c3ee1f708e5e0b372fd972c9e73fe3c6931f`  
		Last Modified: Mon, 01 Sep 2025 22:31:51 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:2090644e2273e294a1b163b6c6f41540d1d197615703cea04df60286da51f185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3353578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa275c6026465a55bc377f6facb26e86dcd47687dd707f66bbd9ca2d9edd789b`

```dockerfile
```

-	Layers:
	-	`sha256:75ac213a4fce41d283121567686347e62f02a0f965432531f28f2dc98a2878a5`  
		Last Modified: Tue, 02 Sep 2025 00:45:51 GMT  
		Size: 3.3 MB (3321018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2794d745c1764fec39ac34e2aa09421c2492d53fc296b7c8610efde123dc4a6`  
		Last Modified: Tue, 02 Sep 2025 00:45:52 GMT  
		Size: 32.6 KB (32560 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:2df270741ef2b8ff2bf4419a171aa1a63f0ff7602fb3ebb3c0e0e7583c371629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188005090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a94f7edfe8f77d4ebcf7e038c14a3d59c376d7abc45824069f224c34aa500b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2146ee5f8688ddaedbf432d5fdd81fdf801bc3702e1e4b1e88ccfe6742af7a85`  
		Last Modified: Fri, 29 Aug 2025 03:00:12 GMT  
		Size: 48.9 MB (48875724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a90f450bb70e1d8fb674b697d35665d29a8ff90d6889c7fd2eb35cb36605b9`  
		Last Modified: Fri, 29 Aug 2025 03:00:15 GMT  
		Size: 1.3 MB (1260558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c515feca2377d2626fa88b713494163a1cdff1171c103499951cd48af4b526`  
		Last Modified: Fri, 29 Aug 2025 03:00:17 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7ff7a2ec4d0e3047b7a7c53df837a2614e2888e24704026f2e384898b6ff5c`  
		Last Modified: Fri, 29 Aug 2025 03:18:13 GMT  
		Size: 766.1 KB (766090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4176a4ddf49558e4f9a77dceb3c7200d8f2141ecd342ba74f3efe31310731473`  
		Last Modified: Fri, 29 Aug 2025 03:18:13 GMT  
		Size: 1.1 MB (1086412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e2e78445aa3c6790af4ab280ae91842d700ccd3f154ff4776614a5eb10476e`  
		Last Modified: Fri, 29 Aug 2025 03:18:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a668c2aa22f30b84bc6fb72336e7d05a2650b67260fd1ca4e2045752fc7e6d`  
		Last Modified: Fri, 29 Aug 2025 03:18:15 GMT  
		Size: 11.6 MB (11641134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f60f74825c23e099c3ba3c72006a3763b5e14814c30f0adb88b5ad26c0c645`  
		Last Modified: Mon, 01 Sep 2025 22:36:56 GMT  
		Size: 120.9 MB (120873079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3c1ec5818d3312109d88fd1e3dfe43537b9e0a108357159f427cebeafc3538`  
		Last Modified: Mon, 01 Sep 2025 22:36:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:c4b2dce4bf29921cedde2675784e7564e5618e20aebf587bf33d78852158d176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 KB (32473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c72f0d411e8410ce3acf99d574ecbc320ec7ddebf994ff20097f98ac9dd4c30`

```dockerfile
```

-	Layers:
	-	`sha256:1c3f1617c6df473c4b90ab5e39d5c2a6fe58cc334101d7c24e9cd01b12ba5a05`  
		Last Modified: Tue, 02 Sep 2025 00:45:56 GMT  
		Size: 32.5 KB (32473 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:1d891cc1fb7d8e7c8dd6b11337dd72e5265da0aac33c3096c224d8011426a04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186696080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432fc1a614e658f0b1edf4dda8097ed0b7ae9deac05872975da47d7abac8e74d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51a2ac9172cb928c21dfc13a44f44b5384646406904cbcf5cb5447f055a6faf`  
		Last Modified: Fri, 29 Aug 2025 02:40:14 GMT  
		Size: 48.2 MB (48205971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b346b9ed64232e8d2bf037abd74ba34428edf2022d9bfa4bad64bc663bee4afa`  
		Last Modified: Fri, 29 Aug 2025 02:40:09 GMT  
		Size: 1.3 MB (1260552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fce96b00aee190cd46335d78779e1b47369fe89758c84233632c09c72fca0a8`  
		Last Modified: Fri, 29 Aug 2025 02:40:09 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db594930f7577a6b22a63655fbaa30de582dcf6b9594e3d5285b1d62e3311ab`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 701.5 KB (701476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2096210d0c248b340441ad5727367aacda7d36b96a87fe37a9f35991277b2636`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 1.1 MB (1086412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e2384ad611ca10466ae91eade4ce3cade33bb653f6c94ccb92c82bd7528dce`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd553ef835b77c52adebbc84428e3e1ad25023b611483b6fb55f6499b6ea4a25`  
		Last Modified: Fri, 29 Aug 2025 03:54:42 GMT  
		Size: 11.6 MB (11639252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e717a4dd3bdd4a20e0952069adf62e603539f8957181fcd65e1a6b73a2af39b3`  
		Last Modified: Mon, 01 Sep 2025 22:42:53 GMT  
		Size: 120.6 MB (120582192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667b1194461d829cefa3742b161e30635424106914d3edc32f671d327a8672d0`  
		Last Modified: Mon, 01 Sep 2025 22:42:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:244b91b2e350fca49aa385b9cd2e56a5486f97fd181b2db27495fa0558843429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3350731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791c2b8f0cb42980186a4beb8d0c61e0797425eab06eebd5e97dfa5d63a3a8e8`

```dockerfile
```

-	Layers:
	-	`sha256:ca6fad082a44e5495954aa768eac41d5b144f7de9b42467efdb6d7191bab4169`  
		Last Modified: Tue, 02 Sep 2025 00:46:00 GMT  
		Size: 3.3 MB (3318043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ce9bb40338deebe5eb758493429f77764f401f5d9e0c44d7fc0777815cfef9`  
		Last Modified: Tue, 02 Sep 2025 00:46:01 GMT  
		Size: 32.7 KB (32688 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0e6454198e858df07560da9e990be5cb4d051145059daff62fda9d3c572363bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 MB (199557367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec528d3e8439c0ba5bc9e05aa0783624295eb3ae9ea287cc99bdf31892d820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b2eb68fe2dae8c7a7d27255a4fcff6292179a6089835879932b2641aad0bc9d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f45584a4c7a524e89b17213975d95dc9685cb0772da9368cb9c503770929cc`  
		Last Modified: Fri, 29 Aug 2025 01:25:44 GMT  
		Size: 50.3 MB (50301989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59516805c8635bd1d480d499042139bd7c135504095064ad26bb40302362ba61`  
		Last Modified: Fri, 29 Aug 2025 01:25:35 GMT  
		Size: 1.3 MB (1260576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0ef24f8fa23e77bc52551102b97ad4c00c4002412fd07b775bc3bf380ce272`  
		Last Modified: Fri, 29 Aug 2025 01:25:36 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1d4dd042ca3ee03655bd48d3301e60231319b4c9c9c985746ef53aaaa53fd9`  
		Last Modified: Fri, 29 Aug 2025 02:41:39 GMT  
		Size: 838.6 KB (838567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ec88dceaa42482ac7f2bad84002257eb8b6d56c65640a08a8ec003f5a99f89`  
		Last Modified: Fri, 29 Aug 2025 02:41:39 GMT  
		Size: 1.0 MB (1046735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61833974c4c0d23d6d38c884bbb5a8f926e832c46df98a7bbc8e23d2e909eecd`  
		Last Modified: Fri, 29 Aug 2025 02:41:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede081c9e5040427f30e26aeffdeabe4c80d51f9342a638603049878ba44552e`  
		Last Modified: Fri, 29 Aug 2025 02:41:41 GMT  
		Size: 11.7 MB (11650068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ce3cddce6ba7d99f36157a31d0cfe5694f17736ba959e6f7c20555ae66bf98`  
		Last Modified: Tue, 02 Sep 2025 00:45:58 GMT  
		Size: 130.3 MB (130327494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5080ffed4a8ebe32c590140e583d6ccf383301d98d3bfe02f03f7e9e82941fc2`  
		Last Modified: Mon, 01 Sep 2025 22:36:03 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:9e000df025b8c20aeb83dbd155e374734e17c99783bf3ff043e9c286c2cac7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3353849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb072d52e35d7a9ce8ff32a4e2ea0c2ba58f8f6b8f8c39be37fa0a54aa0328b4`

```dockerfile
```

-	Layers:
	-	`sha256:25a58b6f8d49541db4e4b56c4bb612094f3dfd1a17d606fb9fe9e3e77ef1e00e`  
		Last Modified: Tue, 02 Sep 2025 00:46:06 GMT  
		Size: 3.3 MB (3321126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3209e7af465e528a20ef16bb19b1e645c3653888e5f70f8250c7c60b693c82a`  
		Last Modified: Tue, 02 Sep 2025 00:46:07 GMT  
		Size: 32.7 KB (32723 bytes)  
		MIME: application/vnd.in-toto+json

## `ghost:latest`

```console
$ docker pull ghost@sha256:2faf7cda2bfe29e925e30e14bed5250c6e326c7653a95e9358ff362717dc5b16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ghost:latest` - linux; amd64

```console
$ docker pull ghost@sha256:d2254b21222cfabdc215b43c92ac189c2351439a40ecdc83a41700f015f2b20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211763653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19035ba1f754fb7e686e3ead03ac05371fb6ebcb5a594235bb2c1c5cfcbd007d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291fc5dbbd39fe685232627c96a45e68110c8aa46cb7b065f3a72e72cb22c31d`  
		Last Modified: Thu, 28 Aug 2025 23:34:31 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2561d51a4c67aeb839775fbbf9f06e9b8f865499c3974f3b15d8748dcb0760a1`  
		Last Modified: Thu, 28 Aug 2025 23:34:37 GMT  
		Size: 49.0 MB (49010562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e06c1a47e17a8b62c4f581dfdec846741e13dbf17aacd62f8afa6d668d3da31`  
		Last Modified: Thu, 28 Aug 2025 23:34:30 GMT  
		Size: 1.7 MB (1712554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2403c8b76caca8d2d0a53ca1ee2475bbaece39b293a49cfba277b01186986bb8`  
		Last Modified: Thu, 28 Aug 2025 23:34:30 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76afcf2fa61fa51d34175604b2d563cce965bdb65b1c28ffb73a1ebc63e6336`  
		Last Modified: Mon, 01 Sep 2025 22:31:05 GMT  
		Size: 1.4 MB (1444945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799552c8963493fd20a6604b1b78f4ee50584bd1d896cc157402c8077ff42996`  
		Last Modified: Mon, 01 Sep 2025 22:31:09 GMT  
		Size: 11.7 MB (11650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c19a50e28a047b135e0e3ffe1247bfe04bd0fab6bac5514fc9af7d154ec8565`  
		Last Modified: Mon, 01 Sep 2025 22:31:12 GMT  
		Size: 119.7 MB (119710178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bc276376483c6b837fa4a33a535ec5c7d285e6d1bfabbfcfdcdecf51cb6f3a`  
		Last Modified: Mon, 01 Sep 2025 22:31:05 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:b27a6f3720b8114a95d861609f204edb6ef9bd73fae96181e1a5dd45f9fb78e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a940a71b4fd4b3556eb01803ecb6e63b108795778c8545326b7c716c280201f7`

```dockerfile
```

-	Layers:
	-	`sha256:de464b26004e59cf977beb0f3cdaaff38e6b4f0833e766b1c0c2b047b89ab118`  
		Last Modified: Tue, 02 Sep 2025 00:45:38 GMT  
		Size: 5.5 MB (5532017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7237eef19ee9904fb66b59c2b8a3ea69d8f40436b916f5b639aeb4741b3a350b`  
		Last Modified: Tue, 02 Sep 2025 00:45:39 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:854fbd11e88160c51d9a2d06fe427d25c19c80cf285926b4fdd1bbecdc091f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203413730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd85aabdfbec73ec1790a771dee3d12061381067e87ad6b49b27cf1a6791172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae1e510a43ef8f416095b11f0182b2e280a16abb567ffe9973ee818f1ced070`  
		Last Modified: Wed, 13 Aug 2025 00:43:01 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5468eccc738adf70ee011b01680c456e47dc04f006dcce1b4cadbf6400263`  
		Last Modified: Fri, 29 Aug 2025 02:42:57 GMT  
		Size: 43.9 MB (43916785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb4b0ef6c2bf4f00b489a41c59c1355636508ad8cc8b009def82424800f2d4c`  
		Last Modified: Fri, 29 Aug 2025 02:42:50 GMT  
		Size: 1.7 MB (1712767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1951b39ccaea6be1c5650f48794d2610c4850f7643d2fbdecbabe1dbb6132054`  
		Last Modified: Fri, 29 Aug 2025 02:42:50 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17358ce1624416ef9ff445daec0c5f9d8b56d0dcf1ca981b81d3ad7fdfddfd0b`  
		Last Modified: Fri, 29 Aug 2025 03:47:51 GMT  
		Size: 1.4 MB (1412627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fb3436b4dbb0037988c989c6e85ea687ab350bd9981dbf00903c477c8bafd1`  
		Last Modified: Fri, 29 Aug 2025 03:47:52 GMT  
		Size: 11.6 MB (11639485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e3dae8a2aa6764159cd144d209389eff5907f4f61c783aaa231625e7a8d39d`  
		Last Modified: Mon, 01 Sep 2025 22:36:11 GMT  
		Size: 120.8 MB (120788809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad92ebadf2b39d220609d1b3753b850a1fff3f9a0944a8920801d6ec17ebb6c`  
		Last Modified: Mon, 01 Sep 2025 22:35:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:9529ba666cb089cbee4321c0a853bbfea116482f0bfc39f0ea1d1f6cefdd5b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5564472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbd7cc01bc0a0f2f594146227aff39025b56fa682086132a547991bcd6afdbb`

```dockerfile
```

-	Layers:
	-	`sha256:bf14bc68813c966bbe8b2bf1ff2923aec3ecf68f0da115ce283156657960bc21`  
		Last Modified: Tue, 02 Sep 2025 00:45:44 GMT  
		Size: 5.5 MB (5534784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed46868ea90f3e5060df97e4ec073c47e70f770d42b0965956af5f8151ef7c0`  
		Last Modified: Tue, 02 Sep 2025 00:45:45 GMT  
		Size: 29.7 KB (29688 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:c71869bc85c04ac42db2d0206a23e0a0012e5dd2a6f3a8bad441bbadc3366b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211307491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d142eaca1b337deba2b831de051dfc274ac02c6088a19dfac39171a950b5f0c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27263372d67228bb86c6e522c8fc32c5e6a4a10ddabec215fa8026f3d01a3508`  
		Last Modified: Thu, 28 Aug 2025 14:40:51 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00ca1ce1c92f9f6153143bddfb381c493c0ae26d3bb85f10d228009ea618291`  
		Last Modified: Fri, 29 Aug 2025 01:27:40 GMT  
		Size: 48.7 MB (48681521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cceee3ed04b670a81910ab2d6400463c1c5253f81047942e7ca695dcbc42bef6`  
		Last Modified: Fri, 29 Aug 2025 01:27:34 GMT  
		Size: 1.7 MB (1712586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9a72dac5922748758980697ec36ffe4814be2e61e21f88b48746e419444192`  
		Last Modified: Fri, 29 Aug 2025 01:27:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990af4a1d6f18056eb115744e5360b959441c63cdac3679b104c29158bc34c5a`  
		Last Modified: Fri, 29 Aug 2025 03:09:43 GMT  
		Size: 1.4 MB (1376654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f35bbd74cc54bb41d37d13a7d299015b97e9b215c742395b169e75fab70ca9`  
		Last Modified: Fri, 29 Aug 2025 03:09:44 GMT  
		Size: 11.7 MB (11650392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918212475e1250b79cf2897198ed00dab67b0f619e097d00489a59f905971a9b`  
		Last Modified: Mon, 01 Sep 2025 22:30:55 GMT  
		Size: 119.8 MB (119800006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759453b512e79c73dbad92d0db51da292d1b4736fb10a248267fbaa032a39947`  
		Last Modified: Mon, 01 Sep 2025 22:30:46 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:7ac6757f4114dc2990c62dd5793009785278c231ae38937c309497e88d36c4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f006d48f55bac7ca7915e12a9ca6c807b4d456d546d35e00b9b33e08cfb444a`

```dockerfile
```

-	Layers:
	-	`sha256:58e7d0eba6c644e7892aeecab188ec6b2e049a87cf4c7ba3cfbc24f721d37b4d`  
		Last Modified: Tue, 02 Sep 2025 00:45:50 GMT  
		Size: 5.5 MB (5532320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3aebc011dd0ca39b19da637deef8c255e64868975c603c86bd92ce8927eb314`  
		Last Modified: Tue, 02 Sep 2025 00:45:51 GMT  
		Size: 29.7 KB (29719 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; ppc64le

```console
$ docker pull ghost@sha256:684dad988bcc8867ee4f8dfa11a5310eaa7354dee2421b9b7713092f8ab66e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222396476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b174c7af12f48df75f029d34136182a00026b3cb584437bd99f6200273987d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db49890cc93d9412b095c6d9e7c7dcd1224e0b5c93c9c8848c12d48ecffbb89a`  
		Last Modified: Wed, 13 Aug 2025 13:16:33 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708047d400332a3ac027b4da8af825b8849d7cf6154f691f6b57c08995f18d5b`  
		Last Modified: Fri, 29 Aug 2025 00:58:52 GMT  
		Size: 51.9 MB (51930458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2905170ec9992e7f18c8d6a624109158fc4d528bbdc72a2bf3b6b5e54abeecd`  
		Last Modified: Fri, 29 Aug 2025 00:58:41 GMT  
		Size: 1.7 MB (1712753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa037f1a005a1ed7b76333d54b8874e5001c088200f60fdbf7a8bf41820a22b9`  
		Last Modified: Fri, 29 Aug 2025 00:58:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cca12707d80a0959f9c8c27d84527a6f395d044dbde84ed7dd6ac6581b59623`  
		Last Modified: Fri, 29 Aug 2025 02:23:49 GMT  
		Size: 1.4 MB (1366738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69098d5fc0ba8e36a59d67177ecb88d69fdec43caedb993f113cbe9548c40fb3`  
		Last Modified: Fri, 29 Aug 2025 02:23:51 GMT  
		Size: 11.7 MB (11650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad520b7406424dd17210f7bf38ab76bbe9e87b3d7c03bd5014dece708efcc6b`  
		Last Modified: Mon, 01 Sep 2025 22:38:59 GMT  
		Size: 123.7 MB (123658547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6c3733ec0f123b114febfe29247afaf79eddfd4d2dfef91760a3071c6eb2a6`  
		Last Modified: Mon, 01 Sep 2025 22:38:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:c15a40d0d6240f38fbb67240a90432f06cca341a5b354a228eccd789c82f7e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c3c4216defb2246a1484c7c9923c2f4488015e3a0ca0c16da74179c1546e13`

```dockerfile
```

-	Layers:
	-	`sha256:55084258c84cba53b42a3dbd4c90b1e800fcfe8b5b1c6f943be6bfe1cf04681c`  
		Last Modified: Tue, 02 Sep 2025 00:45:56 GMT  
		Size: 5.5 MB (5531874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fc0054474cfcb15ca29acbded12e51e37f28f9ca1066504c1ff4dc22618766d`  
		Last Modified: Tue, 02 Sep 2025 00:45:57 GMT  
		Size: 29.6 KB (29634 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:2fa624f4cf86e0d598710fd73c2f31b01ea41b83e7873a0ef079af1ecfc8a0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213760480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dcfcc37c5081780279297d15452f2a813e05bf8279e865fd109daa980d5b00b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Thu, 28 Aug 2025 22:35:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV NODE_VERSION=22.19.0
# Thu, 28 Aug 2025 22:35:08 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 28 Aug 2025 22:35:08 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 22:35:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 22:35:08 GMT
CMD ["node"]
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GOSU_VERSION=1.17
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV NODE_ENV=production
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 29 Aug 2025 20:19:14 GMT
ENV GHOST_VERSION=6.0.6
# Fri, 29 Aug 2025 20:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
WORKDIR /var/lib/ghost
# Fri, 29 Aug 2025 20:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 29 Aug 2025 20:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 29 Aug 2025 20:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 20:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 29 Aug 2025 20:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dadfc3ada3cd4f49e71dc39867db6cf8d4c2cb806f817ea84710057fd1995b`  
		Last Modified: Wed, 13 Aug 2025 15:28:53 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3522eaaadd5604724d773f31f0376394ec59311b336e319267f643b81cd1051`  
		Last Modified: Fri, 29 Aug 2025 03:44:00 GMT  
		Size: 49.2 MB (49213158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc48901f36b0038823fc66a587782bcd79cd29b262bcdeb54ca8a5d8c38241e7`  
		Last Modified: Fri, 29 Aug 2025 03:43:57 GMT  
		Size: 1.7 MB (1712574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64fe4de3e909696bcb9189e0e6e5386374bc317fef0b4f298fc25104f773f5b`  
		Last Modified: Fri, 29 Aug 2025 03:43:57 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610d989a0365953e0828dcbe697cab36bb0360cbb7bc554bde86f42117518fac`  
		Last Modified: Fri, 29 Aug 2025 04:16:33 GMT  
		Size: 1.4 MB (1410318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf7402bf0405eabcf9ff96b07bf7f50c5a61dc63f676c13c6609f4a82130c6b`  
		Last Modified: Fri, 29 Aug 2025 04:16:33 GMT  
		Size: 11.7 MB (11665019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186feb277d2b3aa866a879927e6ac2a2f055558bb61e62904684010e741d9527`  
		Last Modified: Mon, 01 Sep 2025 22:38:46 GMT  
		Size: 122.9 MB (122867250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f77612ad47a3e7cd7d94544b5b7c12172342ba0a70ef19d3c58a9d99c93ff`  
		Last Modified: Mon, 01 Sep 2025 22:38:41 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:41b9e9b1376b1deaa860ac578c75f1bfe6ba466b97f586953b697f8ba5b4e069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21555f60d49a223816f0075d68a3ee97aed16fcbfc27ed85677741c553ba158a`

```dockerfile
```

-	Layers:
	-	`sha256:613e5cad64b24765f0ee56b712968fe09103676d694c7a0020f2d505cd96504e`  
		Last Modified: Tue, 02 Sep 2025 00:46:02 GMT  
		Size: 5.5 MB (5525844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:035031bf928a9a4cef3690baf6c625f369d7203c6f88c38d7a19215607c48b96`  
		Last Modified: Tue, 02 Sep 2025 00:46:03 GMT  
		Size: 29.6 KB (29586 bytes)  
		MIME: application/vnd.in-toto+json

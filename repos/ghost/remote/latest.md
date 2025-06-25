## `ghost:latest`

```console
$ docker pull ghost@sha256:80e0e29b9c0dc625e7ab6499662c616ed2badebb5b09512840f7de3aebba13b7
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
$ docker pull ghost@sha256:1893eedc3b74fe2e26c42fbdd60b5a04039f059cf1d3641b6508e37bd8da0347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189604576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3872058e77ecf4e39625bda0fab8e517c93d1d1ec15b603aaa100c6aa868df3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Mon, 23 Jun 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
ENV NODE_VERSION=20.19.3
# Mon, 23 Jun 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Mon, 23 Jun 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 10:06:16 GMT
CMD ["node"]
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 24 Jun 2025 14:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
ENV NODE_ENV=production
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Tue, 24 Jun 2025 14:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_VERSION=5.127.1
# Tue, 24 Jun 2025 14:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
WORKDIR /var/lib/ghost
# Tue, 24 Jun 2025 14:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 24 Jun 2025 14:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Jun 2025 14:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 24 Jun 2025 14:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8378ad7fe587196cf9250457c2ebecaea9ab60a938f903da704f1a091b0e1134`  
		Last Modified: Mon, 23 Jun 2025 12:59:59 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c8d5f01aa7889c1ad87a52b5d91f95afff417add63875f42a11bafdfd596f8`  
		Last Modified: Mon, 23 Jun 2025 13:07:23 GMT  
		Size: 41.2 MB (41204731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f1c9356ab294ea2d99ba0a2bada9feb13f7e593b2948910467cc20bcb086b5`  
		Last Modified: Mon, 23 Jun 2025 13:00:13 GMT  
		Size: 1.7 MB (1712532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4104b2adf35f2212a0789a4d260bf9edb5d62bc9630f5357d24c3f313a38c5`  
		Last Modified: Mon, 23 Jun 2025 13:00:25 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8c9a3fbdb16b0e4dec0c699a7838e58095f6dc4f3856df0596ef48b9469aab`  
		Last Modified: Tue, 24 Jun 2025 18:18:43 GMT  
		Size: 1.4 MB (1444953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b13f6113bf91b3ee0b5747f7d18cb77f5989d1b3d8a425b272fcb60fdac531`  
		Last Modified: Tue, 24 Jun 2025 18:45:32 GMT  
		Size: 11.1 MB (11128982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b0137109f20e365a14e8cdcebef2c4b85be4a3b4177a9d7b41edf2757384f5`  
		Last Modified: Tue, 24 Jun 2025 18:45:49 GMT  
		Size: 105.9 MB (105878915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a512513981542e225a69af8bfa24ee75a11eddaa7c28d103e4bf533e467fc12`  
		Last Modified: Tue, 24 Jun 2025 18:45:33 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:5aa5629e4c4714397d80962a44f4d04da18527d52943180354b2fb8e538c12a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c64491af58bb2b29215ab417119d51d5a94b7330d20177c4263cee15f323f44`

```dockerfile
```

-	Layers:
	-	`sha256:46fdc167e59da209ab45bb5a5377bdd8af174d32fbf5acb1b352236ed4d4b049`  
		Last Modified: Tue, 24 Jun 2025 18:45:27 GMT  
		Size: 5.5 MB (5516637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b100dce2d0e97f29f8bf7ed58d886e8ce3a303cf5abfc1e5f9d8e5ede322f35c`  
		Last Modified: Tue, 24 Jun 2025 18:45:28 GMT  
		Size: 29.3 KB (29309 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm variant v7

```console
$ docker pull ghost@sha256:298e9503aba64930c3264e13c96327de6a48e645c8e491bdb6e30e68d7c2b641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192886702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75daa7299a9d37a5017018b5cac3ea7b500df4b887427a0963920ef27ab73e12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Mon, 23 Jun 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
ENV NODE_VERSION=20.19.3
# Mon, 23 Jun 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Mon, 23 Jun 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 10:06:16 GMT
CMD ["node"]
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 24 Jun 2025 14:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
ENV NODE_ENV=production
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Tue, 24 Jun 2025 14:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_VERSION=5.127.1
# Tue, 24 Jun 2025 14:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
WORKDIR /var/lib/ghost
# Tue, 24 Jun 2025 14:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 24 Jun 2025 14:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Jun 2025 14:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 24 Jun 2025 14:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be49c2d8de46a8a7413b09db3e85d95aa81164971e17f57e239112e60c445422`  
		Last Modified: Wed, 11 Jun 2025 05:35:31 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b95ffd449a14d69dc2800d772bcc0bc0d3a08fa4e8612d3f9b9fc1842b9d2b7`  
		Last Modified: Mon, 23 Jun 2025 14:42:59 GMT  
		Size: 37.3 MB (37275430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2121d77b014c5403f5f0b53bd398ea9a99b3f1e19289db3c69852f6a87002fdf`  
		Last Modified: Mon, 23 Jun 2025 14:42:34 GMT  
		Size: 1.7 MB (1712721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09feb4ca3005e4ad24e71acf3976485e054a46e15c1635904abf6a6a2762332`  
		Last Modified: Mon, 23 Jun 2025 14:42:37 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ae9dc89e25ecc1916883627ea4b2eeb86a018ed3357338d183f72598357d42`  
		Last Modified: Mon, 23 Jun 2025 15:16:20 GMT  
		Size: 1.4 MB (1412613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0374acc8a05e0b52bf616851e57f22b5e16db2664694e24734f219fb2c48f33d`  
		Last Modified: Mon, 23 Jun 2025 15:16:21 GMT  
		Size: 11.1 MB (11128475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0b646359eeb9ae2dd0f986402742a21248e28246d414c0f20a02e1c4be3f4`  
		Last Modified: Tue, 24 Jun 2025 22:50:35 GMT  
		Size: 117.4 MB (117414384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c58a49612a94508ff655e24cfcf04e1a2aa8a215110c26b169d1274a746b2eb`  
		Last Modified: Tue, 24 Jun 2025 22:50:22 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:fdcf603b8e5e25c50238460987b037209a9733e89e24eeed3ad4b05023d819ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f527177b748553d9911b121d4f02d857bba0a434fb4e19bc1fd58b0d224a1032`

```dockerfile
```

-	Layers:
	-	`sha256:eeb0a7dbc0f98e6735d640478035197d4d1b83dea1abeb8f4b2f3331b72c3c65`  
		Last Modified: Tue, 24 Jun 2025 21:45:27 GMT  
		Size: 5.5 MB (5519400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df2f320ea5be0884735587de6c640a7170c9223c6a7abc48960e008d48f3fac`  
		Last Modified: Tue, 24 Jun 2025 21:45:27 GMT  
		Size: 29.4 KB (29411 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:0bdb3a5b3da8cb4c841ee8529daa1ab841776d9e66502333d279a2198f548ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189427761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc1fd79c2fa24ec39ee42e374fa55ca867cc4261e15e094c76e43ca97fef69d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Mon, 23 Jun 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
ENV NODE_VERSION=20.19.3
# Mon, 23 Jun 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Mon, 23 Jun 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 10:06:16 GMT
CMD ["node"]
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 24 Jun 2025 14:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
ENV NODE_ENV=production
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Tue, 24 Jun 2025 14:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_VERSION=5.127.1
# Tue, 24 Jun 2025 14:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
WORKDIR /var/lib/ghost
# Tue, 24 Jun 2025 14:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 24 Jun 2025 14:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Jun 2025 14:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 24 Jun 2025 14:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77a0ca239ad308830036884055148fca700796ec3a5ea254e2120fd87181df3`  
		Last Modified: Mon, 23 Jun 2025 13:45:25 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919c41f229acf793707f728db38da4ffdf09dbd2b8e720b9e4d0177fe3d7198f`  
		Last Modified: Mon, 23 Jun 2025 13:45:28 GMT  
		Size: 41.2 MB (41153509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0c5d6a054e3be8b1583d3ff6d64de3813bf66a0ef5248e10d0a522d8ff1482`  
		Last Modified: Mon, 23 Jun 2025 13:45:26 GMT  
		Size: 1.7 MB (1712588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a707d65b9b92ce89cafae5e0e461c579d36032f74dcaa248f6f0d0947372787f`  
		Last Modified: Mon, 23 Jun 2025 13:45:24 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6add438f81dcf0781b36da4950f6aeb9937d5acb8a8efff3b3d5c92517ec6fb`  
		Last Modified: Mon, 23 Jun 2025 14:12:48 GMT  
		Size: 1.4 MB (1376671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2bd69f741afb60e80dcbb24dd7e862ad0408984fb8b304b0bb356f95233f74`  
		Last Modified: Mon, 23 Jun 2025 14:12:49 GMT  
		Size: 11.1 MB (11128146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b4d7c7e72d07cac725fa0fa371710dc07c947c8a5cca78506c80f46d51629a`  
		Last Modified: Tue, 24 Jun 2025 18:18:42 GMT  
		Size: 106.0 MB (105974839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376648f5eda1fc2905be7610856f8311ff668aa999d1760a5cff110a26d88a19`  
		Last Modified: Tue, 24 Jun 2025 18:18:34 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:faf8873654734a994d4a52328cbfce7fe9697b602e3776cc06014e68070a9a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8728820e7e55a30297bbd0ab6fd4d0937f62839a88928c468fdcd65f11a08cbc`

```dockerfile
```

-	Layers:
	-	`sha256:208d1d3f3c2cb0f8f1afe1592ad0a22374eaae5456d704c7550620f8de6bcb4e`  
		Last Modified: Tue, 24 Jun 2025 18:45:36 GMT  
		Size: 5.5 MB (5516940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8855d00ba43515800d4e26c6ade596015fe7d88c64f1539323d3af58b3d5890a`  
		Last Modified: Tue, 24 Jun 2025 18:45:37 GMT  
		Size: 29.4 KB (29443 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; ppc64le

```console
$ docker pull ghost@sha256:64376c22f1e44863df9aed75257ca4178ce00aec23e3f697e800f251cb794e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210347387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b9192e5d307d1f4df68436eee29185d10297248d99045762542673087352f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Mon, 23 Jun 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
ENV NODE_VERSION=20.19.3
# Mon, 23 Jun 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Mon, 23 Jun 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 10:06:16 GMT
CMD ["node"]
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 24 Jun 2025 14:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
ENV NODE_ENV=production
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Tue, 24 Jun 2025 14:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_VERSION=5.127.1
# Tue, 24 Jun 2025 14:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
WORKDIR /var/lib/ghost
# Tue, 24 Jun 2025 14:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 24 Jun 2025 14:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Jun 2025 14:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 24 Jun 2025 14:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593370f5b2fddf3c107ef6b92f1ac55675d3ca666b181f720d05e19519d6e87c`  
		Last Modified: Wed, 11 Jun 2025 05:18:18 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d8f5206cfc8b74e0ce42fe5725be29628fdb055dc92aa47632164c28b40e23`  
		Last Modified: Mon, 23 Jun 2025 15:51:15 GMT  
		Size: 43.7 MB (43721422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f413f9548e340a6b6394c25b5a23f998a1c6326ae806fe0ee92fae8e2c2089`  
		Last Modified: Mon, 23 Jun 2025 13:33:14 GMT  
		Size: 1.7 MB (1712693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d0da99e1486d93650a00aa9a8da12c41e46706394c78e0b2aaa9f20bf3a75d`  
		Last Modified: Mon, 23 Jun 2025 13:33:20 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5c6db40db777cd02144515c85651931c05c9316776540aaa2ceb650d5f1a9`  
		Last Modified: Mon, 23 Jun 2025 14:18:59 GMT  
		Size: 1.4 MB (1366721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdb03e14d3349cddc25d10e5b9fc83c4d553bfb8136c162821e18500d090250`  
		Last Modified: Mon, 23 Jun 2025 14:19:00 GMT  
		Size: 11.1 MB (11132108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5227b511ff200ef716b2fba85507372318f4f7dfdabc6d3898702f875c4ff3f5`  
		Last Modified: Tue, 24 Jun 2025 18:26:15 GMT  
		Size: 120.3 MB (120337315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1539f3e68b098a0025afffe9c722da4506305725566ac12931b63c5fcc4e7d8`  
		Last Modified: Tue, 24 Jun 2025 18:26:07 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:897aea28fdf8d248bbf230c4c6c53eda388841636c44ec1a446241bc22187943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ca9927af8f388ecc159949a3891c1e8eb9a6e8b69e41f52dd1d8c2adbb8e86`

```dockerfile
```

-	Layers:
	-	`sha256:0a80bb4582ae1f777ca42f042458c1c2f670b5872a7d55d7db4a40a64e7c6636`  
		Last Modified: Tue, 24 Jun 2025 21:45:36 GMT  
		Size: 5.5 MB (5516488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e25ad1012e10d32dca0b0acaf2d0a8c134f18a6969e7f69609eb84da15f814c9`  
		Last Modified: Tue, 24 Jun 2025 21:45:37 GMT  
		Size: 29.4 KB (29357 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:6e9bb5b6b353b16311df2c1d8231964b78ff80f86730119e6a5ae9f1ab1ccf50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202095327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b27884c13e7c11cc3caf47ca1267ebe7b93ca4f692a838aee912cfdc53397a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Mon, 23 Jun 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
ENV NODE_VERSION=20.19.3
# Mon, 23 Jun 2025 10:06:16 GMT
RUN ARCH= OPENSSL_ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64' OPENSSL_ARCH='linux-x86_64';;       ppc64el) ARCH='ppc64le' OPENSSL_ARCH='linux-ppc64le';;       s390x) ARCH='s390x' OPENSSL_ARCH='linux*-s390x';;       arm64) ARCH='arm64' OPENSSL_ARCH='linux-aarch64';;       armhf) ARCH='armv7l' OPENSSL_ARCH='linux-armv4';;       i386) ARCH='x86' OPENSSL_ARCH='linux-elf';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -ex     && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr xz-utils libatomic1 --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;     && apt-mark auto '.*' > /dev/null     && find /usr/local -type f -executable -exec ldd '{}' ';'       | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'       | sort -u       | xargs -r dpkg-query --search       | cut -d: -f1       | sort -u       | xargs -r apt-mark manual     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && ln -s /usr/local/bin/node /usr/local/bin/nodejs     && node --version     && npm --version     && rm -rf /tmp/* # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Mon, 23 Jun 2025 10:06:16 GMT
RUN set -ex   && savedAptMark="$(apt-mark showmanual)"   && apt-get update && apt-get install -y ca-certificates curl wget gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apt-mark auto '.*' > /dev/null   && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; }   && find /usr/local -type f -executable -exec ldd '{}' ';'     | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'     | sort -u     | xargs -r dpkg-query --search     | cut -d: -f1     | sort -u     | xargs -r apt-mark manual   && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 10:06:16 GMT
CMD ["node"]
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 24 Jun 2025 14:19:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
ENV NODE_ENV=production
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_CLI_VERSION=1.27.0
# Tue, 24 Jun 2025 14:19:14 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Tue, 24 Jun 2025 14:19:14 GMT
ENV GHOST_VERSION=5.127.1
# Tue, 24 Jun 2025 14:19:14 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		savedAptMark="$(apt-mark showmanual)"; 	aptPurge=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		aptPurge=1; 		apt-get update; 		apt-get install -y --no-install-recommends g++ make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			aptPurge=1; 			apt-get update; 			apt-get install -y --no-install-recommends g++ make python3; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.10 in Debian bullseye is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$aptPurge" ]; then 		apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 		rm -rf /var/lib/apt/lists/*; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
WORKDIR /var/lib/ghost
# Tue, 24 Jun 2025 14:19:14 GMT
VOLUME [/var/lib/ghost/content]
# Tue, 24 Jun 2025 14:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Jun 2025 14:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Jun 2025 14:19:14 GMT
EXPOSE map[2368/tcp:{}]
# Tue, 24 Jun 2025 14:19:14 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78e77692ee2ff62ecac2703b5f48519067db7c167af6d261258de5133878d79`  
		Last Modified: Wed, 11 Jun 2025 03:07:44 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fedd4346027d0c91eb2d1ee461d202d1f1c9b721486d3e79dc0fa17288ee6445`  
		Last Modified: Mon, 23 Jun 2025 14:12:43 GMT  
		Size: 41.4 MB (41439069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1e9d7aef17e8da4144f40aa9870b33fea5adb93ccdd432519b68ffca491111`  
		Last Modified: Mon, 23 Jun 2025 14:12:40 GMT  
		Size: 1.7 MB (1712554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8216e9f6a84ee12b42c16d1c6c0ea7d8ea28b611e4882c9d63f85719fa1835a7`  
		Last Modified: Mon, 23 Jun 2025 14:12:40 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f87c8dea3161e286dcf106a717dd8dcb84182931a05b071e3fe05b71b23565`  
		Last Modified: Mon, 23 Jun 2025 15:15:12 GMT  
		Size: 1.4 MB (1410199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bde309ce70f83a5cbc82a8380a00b014b9f48b3a06daf2773e06d1bbe6af33`  
		Last Modified: Mon, 23 Jun 2025 15:15:13 GMT  
		Size: 11.1 MB (11127961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a958bf60fbf8c926c8f3924494c68acfc7a05726c7d6215425f0f6de57ce02a1`  
		Last Modified: Tue, 24 Jun 2025 18:23:22 GMT  
		Size: 119.5 MB (119513360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a943eacb3b4f833a0502ed6f9e7a497e207298cff8ca916cfe042399b3199128`  
		Last Modified: Tue, 24 Jun 2025 18:23:13 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:latest` - unknown; unknown

```console
$ docker pull ghost@sha256:6dc2c10ff7ec239685a6fbcc1fce4a55e9d207b9f52242e81ea767ce58b208ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5539770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a147561c49296f40c3126b4e69b3cbf7c2fe21ab8f95e181410f091eec620bd`

```dockerfile
```

-	Layers:
	-	`sha256:497efd18be7c678731642cc7d700dc824d7f591cfb9de231fe16d0e7205ec018`  
		Last Modified: Tue, 24 Jun 2025 18:45:45 GMT  
		Size: 5.5 MB (5510460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f5d170bc90ca3274d63e68a3c0ab81336fa8700eb47828555430a0fdc432a7`  
		Last Modified: Tue, 24 Jun 2025 18:45:46 GMT  
		Size: 29.3 KB (29310 bytes)  
		MIME: application/vnd.in-toto+json
